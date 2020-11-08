---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94193071"
---
# <span data-ttu-id="fbe6b-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="fbe6b-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="fbe6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbe6b-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe6b-103">Ottiene la cronologia degli Smart Group</span><span class="sxs-lookup"><span data-stu-id="fbe6b-103">Gets smart group history</span></span>

## <span data-ttu-id="fbe6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbe6b-104">SYNTAX</span></span>

### <span data-ttu-id="fbe6b-105">BySmartGroupId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fbe6b-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbe6b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fbe6b-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbe6b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbe6b-107">DESCRIPTION</span></span>
<span data-ttu-id="fbe6b-108">Il cmdlet **Get-AzSmartGroupHistory** ottiene la cronologia Smart Group.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="fbe6b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbe6b-109">EXAMPLES</span></span>

### <span data-ttu-id="fbe6b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fbe6b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="fbe6b-111">Ottiene i dettagli della cronologia dei gruppi smart.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-111">Gets smart group history details.</span></span>

## <span data-ttu-id="fbe6b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbe6b-112">PARAMETERS</span></span>

### <span data-ttu-id="fbe6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe6b-113">-DefaultProfile</span></span>
<span data-ttu-id="fbe6b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbe6b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbe6b-115">-InputObject</span></span>
<span data-ttu-id="fbe6b-116">Oggetto di input da pipeline.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="fbe6b-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="fbe6b-117">-SmartGroupId</span></span>
<span data-ttu-id="fbe6b-118">Identificatore univoco di SmartGroup/ResourceId di Alert.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

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

### <span data-ttu-id="fbe6b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe6b-119">CommonParameters</span></span>
<span data-ttu-id="fbe6b-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe6b-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbe6b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe6b-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbe6b-122">INPUTS</span></span>

### <span data-ttu-id="fbe6b-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fbe6b-123">None</span></span>

## <span data-ttu-id="fbe6b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbe6b-124">OUTPUTS</span></span>

### <span data-ttu-id="fbe6b-125">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="fbe6b-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="fbe6b-126">Note</span><span class="sxs-lookup"><span data-stu-id="fbe6b-126">NOTES</span></span>

## <span data-ttu-id="fbe6b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbe6b-127">RELATED LINKS</span></span>