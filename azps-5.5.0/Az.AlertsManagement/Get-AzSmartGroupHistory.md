---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192606"
---
# <span data-ttu-id="35742-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="35742-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="35742-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35742-102">SYNOPSIS</span></span>
<span data-ttu-id="35742-103">Recupera la cronologia intelligente dei gruppi</span><span class="sxs-lookup"><span data-stu-id="35742-103">Gets smart group history</span></span>

## <span data-ttu-id="35742-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35742-104">SYNTAX</span></span>

### <span data-ttu-id="35742-105">BySmartGroupId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="35742-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35742-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="35742-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35742-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="35742-107">DESCRIPTION</span></span>
<span data-ttu-id="35742-108">Il cmdlet **Get-AzSmartGroupHistory ottiene** la cronologia smart group.</span><span class="sxs-lookup"><span data-stu-id="35742-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="35742-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35742-109">EXAMPLES</span></span>

### <span data-ttu-id="35742-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35742-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="35742-111">Recupera dettagli intelligenti della cronologia del gruppo.</span><span class="sxs-lookup"><span data-stu-id="35742-111">Gets smart group history details.</span></span>

## <span data-ttu-id="35742-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35742-112">PARAMETERS</span></span>

### <span data-ttu-id="35742-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35742-113">-DefaultProfile</span></span>
<span data-ttu-id="35742-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35742-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35742-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35742-115">-InputObject</span></span>
<span data-ttu-id="35742-116">Oggetto di input dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="35742-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="35742-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="35742-117">-SmartGroupId</span></span>
<span data-ttu-id="35742-118">Identificatore univoco di SmartGroup/ResourceId dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="35742-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

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

### <span data-ttu-id="35742-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35742-119">CommonParameters</span></span>
<span data-ttu-id="35742-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35742-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35742-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35742-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35742-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="35742-122">INPUTS</span></span>

### <span data-ttu-id="35742-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="35742-123">None</span></span>

## <span data-ttu-id="35742-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35742-124">OUTPUTS</span></span>

### <span data-ttu-id="35742-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="35742-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="35742-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="35742-126">NOTES</span></span>

## <span data-ttu-id="35742-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35742-127">RELATED LINKS</span></span>
