---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475957"
---
# <span data-ttu-id="4a31b-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="4a31b-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="4a31b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a31b-102">SYNOPSIS</span></span>
<span data-ttu-id="4a31b-103">Ottiene informazioni sulla cronologia degli avvisi</span><span class="sxs-lookup"><span data-stu-id="4a31b-103">Gets Alert History information</span></span>

## <span data-ttu-id="4a31b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a31b-104">SYNTAX</span></span>

### <span data-ttu-id="4a31b-105">ByAlertId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a31b-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a31b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4a31b-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a31b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a31b-107">DESCRIPTION</span></span>
<span data-ttu-id="4a31b-108">Il cmdlet **Get-AzAlertObjectHistory** ottiene la cronologia dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4a31b-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="4a31b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a31b-109">EXAMPLES</span></span>

### <span data-ttu-id="4a31b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4a31b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="4a31b-111">Ottiene i dettagli della cronologia degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="4a31b-111">Gets alert history details.</span></span> 

## <span data-ttu-id="4a31b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a31b-112">PARAMETERS</span></span>

### <span data-ttu-id="4a31b-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="4a31b-113">-AlertId</span></span>
<span data-ttu-id="4a31b-114">Identificatore univoco di Alert/ResourceId of Alert.</span><span class="sxs-lookup"><span data-stu-id="4a31b-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="4a31b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a31b-115">-DefaultProfile</span></span>
<span data-ttu-id="4a31b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a31b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a31b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a31b-117">-InputObject</span></span>
<span data-ttu-id="4a31b-118">Oggetto di input da pipeline.</span><span class="sxs-lookup"><span data-stu-id="4a31b-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="4a31b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a31b-119">CommonParameters</span></span>
<span data-ttu-id="4a31b-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a31b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a31b-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a31b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a31b-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a31b-122">INPUTS</span></span>

### <span data-ttu-id="4a31b-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4a31b-123">None</span></span>

## <span data-ttu-id="4a31b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a31b-124">OUTPUTS</span></span>

### <span data-ttu-id="4a31b-125">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="4a31b-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="4a31b-126">Note</span><span class="sxs-lookup"><span data-stu-id="4a31b-126">NOTES</span></span>

## <span data-ttu-id="4a31b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a31b-127">RELATED LINKS</span></span>
