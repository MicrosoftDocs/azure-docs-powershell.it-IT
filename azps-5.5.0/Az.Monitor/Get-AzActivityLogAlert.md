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
ms.locfileid: "100398564"
---
# <span data-ttu-id="8b465-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8b465-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="8b465-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b465-102">SYNOPSIS</span></span>
<span data-ttu-id="8b465-103">Ottiene una o più risorse di avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="8b465-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="8b465-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b465-104">SYNTAX</span></span>

### <span data-ttu-id="8b465-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b465-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b465-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b465-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b465-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8b465-107">DESCRIPTION</span></span>
<span data-ttu-id="8b465-108">Il cmdlet **Get-AzActivityLogAlert** ottiene una o più risorse di avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="8b465-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="8b465-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b465-109">EXAMPLES</span></span>

### <span data-ttu-id="8b465-110">Esempio 1: Ottenere avvisi di un log attività in base all'ID sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="8b465-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="8b465-111">Questo comando elenca tutti gli avvisi del log attività per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="8b465-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="8b465-112">Esempio 2: Ottenere avvisi del log attività per il gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="8b465-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="8b465-113">Questo comando elenca gli avvisi del log attività per il gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="8b465-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="8b465-114">Esempio 3: Ricevere un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="8b465-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="8b465-115">Questo comando elenca un avviso del log attività (un elenco con un singolo elemento).</span><span class="sxs-lookup"><span data-stu-id="8b465-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="8b465-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b465-116">PARAMETERS</span></span>

### <span data-ttu-id="8b465-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b465-117">-DefaultProfile</span></span>
<span data-ttu-id="8b465-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="8b465-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b465-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8b465-119">-Name</span></span>
<span data-ttu-id="8b465-120">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="8b465-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="8b465-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b465-121">-ResourceGroupName</span></span>
<span data-ttu-id="8b465-122">Nome del gruppo di risorse in cui si trova la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="8b465-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="8b465-123">Se Name non è Null o vuoto, questo parametro deve contenere e una stringa non vuota.</span><span class="sxs-lookup"><span data-stu-id="8b465-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="8b465-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b465-124">CommonParameters</span></span>
<span data-ttu-id="8b465-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b465-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b465-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8b465-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b465-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="8b465-127">INPUTS</span></span>

### <span data-ttu-id="8b465-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8b465-128">System.String</span></span>

## <span data-ttu-id="8b465-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b465-129">OUTPUTS</span></span>

### <span data-ttu-id="8b465-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="8b465-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="8b465-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="8b465-131">NOTES</span></span>

## <span data-ttu-id="8b465-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b465-132">RELATED LINKS</span></span>

[<span data-ttu-id="8b465-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8b465-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)


[<span data-ttu-id="8b465-134">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8b465-134">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="8b465-135">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="8b465-135">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="8b465-136">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="8b465-136">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
