---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsoffer
schema: 2.0.0
ms.openlocfilehash: 7b2fcb224486915e78bdd90a84941ac0207a45c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863913"
---
# <span data-ttu-id="d5b6e-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="d5b6e-101">Get-AzsOffer</span></span>

## <span data-ttu-id="d5b6e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b6e-103">Ottenere l'elenco delle offerte pubbliche per il provider radice.</span><span class="sxs-lookup"><span data-stu-id="d5b6e-103">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="d5b6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5b6e-104">SYNTAX</span></span>

```
Get-AzsOffer [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d5b6e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5b6e-105">DESCRIPTION</span></span>
<span data-ttu-id="d5b6e-106">Ottenere l'elenco delle offerte pubbliche per il provider radice.</span><span class="sxs-lookup"><span data-stu-id="d5b6e-106">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="d5b6e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5b6e-107">EXAMPLES</span></span>

### <span data-ttu-id="d5b6e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d5b6e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOffer | fl *

Description : 
DisplayName : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Id          : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Name        : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6

Description : 
DisplayName : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Id          : /delegatedProviders/default/offers/TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Name        : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
```

<span data-ttu-id="d5b6e-109">Ottenere l'elenco delle offerte pubbliche</span><span class="sxs-lookup"><span data-stu-id="d5b6e-109">Get the list of public offers</span></span>

## <span data-ttu-id="d5b6e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5b6e-110">PARAMETERS</span></span>

### <span data-ttu-id="d5b6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5b6e-111">-DefaultProfile</span></span>
<span data-ttu-id="d5b6e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5b6e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d5b6e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b6e-113">CommonParameters</span></span>
<span data-ttu-id="d5b6e-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5b6e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b6e-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5b6e-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b6e-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5b6e-116">INPUTS</span></span>

## <span data-ttu-id="d5b6e-117">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5b6e-117">OUTPUTS</span></span>

### <span data-ttu-id="d5b6e-118">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="d5b6e-118">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="d5b6e-119">Note</span><span class="sxs-lookup"><span data-stu-id="d5b6e-119">NOTES</span></span>

## <span data-ttu-id="d5b6e-120">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5b6e-120">RELATED LINKS</span></span>

