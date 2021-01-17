---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 030564f700f399b1880d36e4dac628a9fc3efa35
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385727"
---
# <span data-ttu-id="6c7e0-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6c7e0-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="6c7e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="6c7e0-103">Ottiene una o più risorse di avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="6c7e0-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="6c7e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c7e0-104">SYNTAX</span></span>

### <span data-ttu-id="6c7e0-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6c7e0-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c7e0-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6c7e0-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c7e0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c7e0-107">DESCRIPTION</span></span>
<span data-ttu-id="6c7e0-108">Il cmdlet **Get-AzActivityLogAlert** ottiene una o più risorse di avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="6c7e0-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="6c7e0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c7e0-109">EXAMPLES</span></span>

### <span data-ttu-id="6c7e0-110">Esempio 1: ottenere avvisi del log attività tramite ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="6c7e0-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="6c7e0-111">Questo comando elenca tutti gli avvisi del log attività per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="6c7e0-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="6c7e0-112">Esempio 2: ottenere avvisi del log attività per il gruppo di risorse specifico</span><span class="sxs-lookup"><span data-stu-id="6c7e0-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="6c7e0-113">Questo comando elenca gli avvisi del log attività per il gruppo di risorse specifico.</span><span class="sxs-lookup"><span data-stu-id="6c7e0-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="6c7e0-114">Esempio 3: ottenere un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="6c7e0-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="6c7e0-115">Questo comando elenca uno (un elenco con un singolo elemento) Avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="6c7e0-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="6c7e0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c7e0-116">PARAMETERS</span></span>

### <span data-ttu-id="6c7e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c7e0-117">-DefaultProfile</span></span>
<span data-ttu-id="6c7e0-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6c7e0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c7e0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c7e0-119">-Name</span></span>
<span data-ttu-id="6c7e0-120">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="6c7e0-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="6c7e0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c7e0-121">-ResourceGroupName</span></span>
<span data-ttu-id="6c7e0-122">Nome del gruppo di risorse in cui è presente la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="6c7e0-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="6c7e0-123">Se nome non è null o vuoto, questo parametro deve contenere una stringa non vuota.</span><span class="sxs-lookup"><span data-stu-id="6c7e0-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="6c7e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c7e0-124">CommonParameters</span></span>
<span data-ttu-id="6c7e0-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c7e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c7e0-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c7e0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c7e0-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c7e0-127">INPUTS</span></span>

### <span data-ttu-id="6c7e0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6c7e0-128">System.String</span></span>

## <span data-ttu-id="6c7e0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c7e0-129">OUTPUTS</span></span>

### <span data-ttu-id="6c7e0-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="6c7e0-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="6c7e0-131">Note</span><span class="sxs-lookup"><span data-stu-id="6c7e0-131">NOTES</span></span>

## <span data-ttu-id="6c7e0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c7e0-132">RELATED LINKS</span></span>

[<span data-ttu-id="6c7e0-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6c7e0-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="6c7e0-134">Update-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6c7e0-134">Update-AzActivityLogAlert</span></span>](./Update-AzActivityLogAlert.md)

[<span data-ttu-id="6c7e0-135">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6c7e0-135">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="6c7e0-136">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="6c7e0-136">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="6c7e0-137">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="6c7e0-137">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
