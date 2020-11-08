---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageacquisition
schema: 2.0.0
ms.openlocfilehash: 098c268d3894d85efe0e17618b5d7ec46b82b0f2
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023219"
---
# <span data-ttu-id="d5bc5-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="d5bc5-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="d5bc5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="d5bc5-103">Restituisce un elenco di acquisizioni BLOB.</span><span class="sxs-lookup"><span data-stu-id="d5bc5-103">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="d5bc5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5bc5-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5bc5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5bc5-105">DESCRIPTION</span></span>
<span data-ttu-id="d5bc5-106">Restituisce un elenco di acquisizioni BLOB.</span><span class="sxs-lookup"><span data-stu-id="d5bc5-106">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="d5bc5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5bc5-107">EXAMPLES</span></span>

### <span data-ttu-id="d5bc5-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="d5bc5-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAcquisition
```

<span data-ttu-id="d5bc5-109">Ottenere l'elenco di BLOB Acquistions.</span><span class="sxs-lookup"><span data-stu-id="d5bc5-109">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="d5bc5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5bc5-110">PARAMETERS</span></span>

### <span data-ttu-id="d5bc5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5bc5-111">-DefaultProfile</span></span>
<span data-ttu-id="d5bc5-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5bc5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5bc5-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d5bc5-113">-Location</span></span>
<span data-ttu-id="d5bc5-114">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d5bc5-114">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d5bc5-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5bc5-115">-SubscriptionId</span></span>
<span data-ttu-id="d5bc5-116">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d5bc5-116">Subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d5bc5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5bc5-117">CommonParameters</span></span>
<span data-ttu-id="d5bc5-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5bc5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5bc5-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5bc5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5bc5-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5bc5-120">INPUTS</span></span>

## <span data-ttu-id="d5bc5-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5bc5-121">OUTPUTS</span></span>

### <span data-ttu-id="d5bc5-122">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IAcquisition</span><span class="sxs-lookup"><span data-stu-id="d5bc5-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IAcquisition</span></span>



## <span data-ttu-id="d5bc5-123">Note</span><span class="sxs-lookup"><span data-stu-id="d5bc5-123">NOTES</span></span>

## <span data-ttu-id="d5bc5-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5bc5-124">RELATED LINKS</span></span>

