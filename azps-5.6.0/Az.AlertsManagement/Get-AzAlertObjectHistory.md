---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: 31b72f68151132fc4dca1bddd18c1a15b6a36f3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961021"
---
# <span data-ttu-id="48ebe-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="48ebe-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="48ebe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="48ebe-103">Recupera informazioni sulla cronologia degli avvisi</span><span class="sxs-lookup"><span data-stu-id="48ebe-103">Gets Alert History information</span></span>

## <span data-ttu-id="48ebe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48ebe-104">SYNTAX</span></span>

### <span data-ttu-id="48ebe-105">ByAlertId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48ebe-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48ebe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="48ebe-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48ebe-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="48ebe-107">DESCRIPTION</span></span>
<span data-ttu-id="48ebe-108">Il cmdlet **Get-AzAlertObjectHistory** ottiene la cronologia degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="48ebe-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="48ebe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48ebe-109">EXAMPLES</span></span>

### <span data-ttu-id="48ebe-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="48ebe-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="48ebe-111">Recupera i dettagli della cronologia degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="48ebe-111">Gets alert history details.</span></span> 

## <span data-ttu-id="48ebe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48ebe-112">PARAMETERS</span></span>

### <span data-ttu-id="48ebe-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="48ebe-113">-AlertId</span></span>
<span data-ttu-id="48ebe-114">Identificatore univoco dell'avviso/ID risorsa dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="48ebe-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48ebe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ebe-115">-DefaultProfile</span></span>
<span data-ttu-id="48ebe-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48ebe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48ebe-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48ebe-117">-InputObject</span></span>
<span data-ttu-id="48ebe-118">Oggetto di input dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="48ebe-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="48ebe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ebe-119">CommonParameters</span></span>
<span data-ttu-id="48ebe-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48ebe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ebe-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48ebe-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ebe-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="48ebe-122">INPUTS</span></span>

### <span data-ttu-id="48ebe-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="48ebe-123">None</span></span>

## <span data-ttu-id="48ebe-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48ebe-124">OUTPUTS</span></span>

### <span data-ttu-id="48ebe-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="48ebe-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="48ebe-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="48ebe-126">NOTES</span></span>

## <span data-ttu-id="48ebe-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48ebe-127">RELATED LINKS</span></span>
