```
fig, axs = plt.subplots(len(contr_levels), len(conditions[::-1]), figsize=[15,15], sharex=True, sharey=True)

for t, x in enumerate(contr_levels):
    for j, c in enumerate(conditions):
        for r in trials:
            spike_times = df[(df.neuron == 'm1_6') & (df.condition == c) & (df.contrast == x) & (df.repetition == r)]['spiketime']
            axs[t, j].vlines(spike_times, r - 0.4, r + 0.4)
        axs[t, j].axvspan(stim_on_time, stim_off_time,
                      alpha= x / (max(contr_levels) * 1.5),
                      color='grey')
        axs[t, j].set_yticks(range(0, 10, 2))
        axs[t, 0].set_ylabel(str(x) + "%")
        axs[t, 1].set_ylabel("Trial Num")
        if t == 0:
            axs[t, 0].set_title('Control Condition', fontsize=10)
            axs[t, 1].set_title('Adaptation Condition', fontsize=10)
        if t == 9:
            axs[t, 1].set_xlabel('Time (ms)')
            axs[t, 0].set_xlabel('Time (ms)')

        
fig.suptitle('m1_6 neuron')
plt.tight_layout()
plt.show()
```
