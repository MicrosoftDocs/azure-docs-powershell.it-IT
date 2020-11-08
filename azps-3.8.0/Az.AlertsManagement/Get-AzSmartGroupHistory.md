---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019161"
---
# <span data-ttu-id="706f3-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="706f3-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="706f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="706f3-102">SYNOPSIS</span></span>
<span data-ttu-id="706f3-103">Ottiene la cronologia degli Smart Group</span><span class="sxs-lookup"><span data-stu-id="706f3-103">Gets smart group history</span></span>

## <span data-ttu-id="706f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="706f3-104">SYNTAX</span></span>

### <span data-ttu-id="706f3-105">BySmartGroupId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="706f3-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="706f3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="706f3-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="706f3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="706f3-107">DESCRIPTION</span></span>
<span data-ttu-id="706f3-108">Il cmdlet **Get-AzSmartGroupHistory** ottiene la cronologia Smart Group.</span><span class="sxs-lookup"><span data-stu-id="706f3-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="706f3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="706f3-109">EXAMPLES</span></span>

### <span data-ttu-id="706f3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="706f3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="706f3-111">Ottiene i dettagli della cronologia dei gruppi smart.</span><span class="sxs-lookup"><span data-stu-id="706f3-111">Gets smart group history details.</span></span>

## <span data-ttu-id="706f3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="706f3-112">PARAMETERS</span></span>

### <span data-ttu-id="706f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="706f3-113">-DefaultProfile</span></span>
<span data-ttu-id="706f3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="706f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706f3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="706f3-115">-InputObject</span></span>
<span data-ttu-id="706f3-116">Oggetto di input da pipeline.</span><span class="sxs-lookup"><span data-stu-id="706f3-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="706f3-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="706f3-117">-SmartGroupId</span></span>
<span data-ttu-id="706f3-118">Identificatore univoco di SmartGroup/ResourceId di Alert.</span><span class="sxs-lookup"><span data-stu-id="706f3-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706f3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="706f3-119">CommonParameters</span></span>
<span data-ttu-id="706f3-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="706f3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="706f3-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="706f3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="706f3-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="706f3-122">INPUTS</span></span>

### <span data-ttu-id="706f3-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="706f3-123">None</span></span>

## <span data-ttu-id="706f3-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="706f3-124">OUTPUTS</span></span>

### <span data-ttu-id="706f3-125">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="706f3-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="706f3-126">Note</span><span class="sxs-lookup"><span data-stu-id="706f3-126">NOTES</span></span>

## <span data-ttu-id="706f3-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="706f3-127">RELATED LINKS</span></span>
