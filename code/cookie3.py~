from __future__ import print_function, division
import thinkbayes2 import Suite

class Cookie(Suite):
	"""A map from string bowl ID to probablity."""

    mixes = {
        'Bowl 1':dict(vanilla=0.75, chocolate=0.25),
        'Bowl 2':dict(vanilla=0.5, chocolate=0.5),
        }

    def Likelihood(self, data, hypo):
        """The likelihood of data under hypothesis.

        data: string cookie type
        hypo: string bowl ID
        """
        mix = self.mixes[hypo]
        like = mix[data]
        return like

def main():
    hypos = ['Bowl 1', 'Bowl 2']

    pmf = Cookie(hypos)

    pmf.Update('vanilla')

    for hypo, prob in pmf.Items():
        print(hypo, prob)


if __name__ == '__main__':
    main()