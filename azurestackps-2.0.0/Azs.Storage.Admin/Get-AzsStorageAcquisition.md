---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageacquisition
schema: 2.0.0
ms.openlocfilehash: 098c268d3894d85efe0e17618b5d7ec46b82b0f2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861661"
---
# <span data-ttu-id="4db5e-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="4db5e-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="4db5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4db5e-102">SYNOPSIS</span></span>
<span data-ttu-id="4db5e-103">Restituisce un elenco di acquisizioni BLOB.</span><span class="sxs-lookup"><span data-stu-id="4db5e-103">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="4db5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4db5e-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4db5e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4db5e-105">DESCRIPTION</span></span>
<span data-ttu-id="4db5e-106">Restituisce un elenco di acquisizioni BLOB.</span><span class="sxs-lookup"><span data-stu-id="4db5e-106">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="4db5e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4db5e-107">EXAMPLES</span></span>

### <span data-ttu-id="4db5e-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="4db5e-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAcquisition
```

<span data-ttu-id="4db5e-109">Ottenere l'elenco di BLOB Acquistions.</span><span class="sxs-lookup"><span data-stu-id="4db5e-109">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="4db5e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4db5e-110">PARAMETERS</span></span>

### <span data-ttu-id="4db5e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db5e-111">-DefaultProfile</span></span>
<span data-ttu-id="4db5e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4db5e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4db5e-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4db5e-113">-Location</span></span>
<span data-ttu-id="4db5e-114">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4db5e-114">Resource location.</span></span>

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

### <span data-ttu-id="4db5e-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4db5e-115">-SubscriptionId</span></span>
<span data-ttu-id="4db5e-116">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4db5e-116">Subscription Id.</span></span>

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

### <span data-ttu-id="4db5e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db5e-117">CommonParameters</span></span>
<span data-ttu-id="4db5e-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4db5e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db5e-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4db5e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db5e-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4db5e-120">INPUTS</span></span>

## <span data-ttu-id="4db5e-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4db5e-121">OUTPUTS</span></span>

### <span data-ttu-id="4db5e-122">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IAcquisition</span><span class="sxs-lookup"><span data-stu-id="4db5e-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IAcquisition</span></span>



## <span data-ttu-id="4db5e-123">Note</span><span class="sxs-lookup"><span data-stu-id="4db5e-123">NOTES</span></span>

## <span data-ttu-id="4db5e-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4db5e-124">RELATED LINKS</span></span>

