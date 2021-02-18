---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 6f171edc1bc9b3d5f4d1f2a5d3ec568fac42929f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409665"
---
# <span data-ttu-id="1eefa-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1eefa-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="1eefa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1eefa-102">SYNOPSIS</span></span>
<span data-ttu-id="1eefa-103">Ottiene una o più risorse di avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="1eefa-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="1eefa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1eefa-104">SYNTAX</span></span>

### <span data-ttu-id="1eefa-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1eefa-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eefa-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1eefa-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1eefa-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1eefa-107">DESCRIPTION</span></span>
<span data-ttu-id="1eefa-108">Il cmdlet **Get-AzActivityLogAlert** ottiene una o più risorse di avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="1eefa-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="1eefa-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1eefa-109">EXAMPLES</span></span>

### <span data-ttu-id="1eefa-110">Esempio 1: Ottenere avvisi di un log attività in base all'ID sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="1eefa-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="1eefa-111">Questo comando elenca tutti gli avvisi del log attività per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="1eefa-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="1eefa-112">Esempio 2: Ottenere avvisi del log attività per il gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="1eefa-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="1eefa-113">Questo comando elenca gli avvisi del log attività per il gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="1eefa-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="1eefa-114">Esempio 3: ricevere un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="1eefa-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="1eefa-115">Questo comando elenca un avviso del log attività (un elenco con un singolo elemento).</span><span class="sxs-lookup"><span data-stu-id="1eefa-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="1eefa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1eefa-116">PARAMETERS</span></span>

### <span data-ttu-id="1eefa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eefa-117">-DefaultProfile</span></span>
<span data-ttu-id="1eefa-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1eefa-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1eefa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1eefa-119">-Name</span></span>
<span data-ttu-id="1eefa-120">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="1eefa-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eefa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eefa-121">-ResourceGroupName</span></span>
<span data-ttu-id="1eefa-122">Nome del gruppo di risorse in cui si trova la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="1eefa-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="1eefa-123">Se Name non è Null o vuoto, questo parametro deve contenere e una stringa non vuota.</span><span class="sxs-lookup"><span data-stu-id="1eefa-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eefa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eefa-124">CommonParameters</span></span>
<span data-ttu-id="1eefa-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eefa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eefa-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1eefa-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eefa-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="1eefa-127">INPUTS</span></span>

### <span data-ttu-id="1eefa-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1eefa-128">System.String</span></span>

## <span data-ttu-id="1eefa-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1eefa-129">OUTPUTS</span></span>

### <span data-ttu-id="1eefa-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="1eefa-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="1eefa-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="1eefa-131">NOTES</span></span>

## <span data-ttu-id="1eefa-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1eefa-132">RELATED LINKS</span></span>

[<span data-ttu-id="1eefa-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1eefa-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)


[<span data-ttu-id="1eefa-134">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1eefa-134">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="1eefa-135">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="1eefa-135">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="1eefa-136">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="1eefa-136">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
