---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 3ad33f83a4e8f96124682bbb189f210f813ead25
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030213"
---
# <span data-ttu-id="5edb6-101">Get-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="5edb6-101">Get-AzsStorageSettings</span></span>

## <span data-ttu-id="5edb6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5edb6-102">SYNOPSIS</span></span>
<span data-ttu-id="5edb6-103">Restituisce le impostazioni del provider di risorse di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5edb6-103">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="5edb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5edb6-104">SYNTAX</span></span>

```
Get-AzsStorageSettings [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5edb6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5edb6-105">DESCRIPTION</span></span>
<span data-ttu-id="5edb6-106">Restituisce le impostazioni del provider di risorse di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5edb6-106">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="5edb6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5edb6-107">EXAMPLES</span></span>

### <span data-ttu-id="5edb6-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="5edb6-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageSettings
```

<span data-ttu-id="5edb6-109">Ottenere le impostazioni di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5edb6-109">Get the storage settings.</span></span>

## <span data-ttu-id="5edb6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5edb6-110">PARAMETERS</span></span>

### <span data-ttu-id="5edb6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5edb6-111">-DefaultProfile</span></span>
<span data-ttu-id="5edb6-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5edb6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5edb6-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5edb6-113">-Location</span></span>
<span data-ttu-id="5edb6-114">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5edb6-114">Resource location.</span></span>

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

### <span data-ttu-id="5edb6-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5edb6-115">-SubscriptionId</span></span>
<span data-ttu-id="5edb6-116">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5edb6-116">Subscription Id.</span></span>

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

### <span data-ttu-id="5edb6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edb6-117">CommonParameters</span></span>
<span data-ttu-id="5edb6-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5edb6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edb6-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5edb6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edb6-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5edb6-120">INPUTS</span></span>

## <span data-ttu-id="5edb6-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5edb6-121">OUTPUTS</span></span>

### <span data-ttu-id="5edb6-122">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="5edb6-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="5edb6-123">Note</span><span class="sxs-lookup"><span data-stu-id="5edb6-123">NOTES</span></span>

## <span data-ttu-id="5edb6-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5edb6-124">RELATED LINKS</span></span>

