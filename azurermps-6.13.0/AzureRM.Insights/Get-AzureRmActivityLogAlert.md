---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: 92550ee9f5eed7cf31624748140a0355ac6849ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687864"
---
# <span data-ttu-id="7f62e-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f62e-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="7f62e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f62e-102">SYNOPSIS</span></span>
<span data-ttu-id="7f62e-103">Ottiene una o più risorse di avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="7f62e-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f62e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f62e-104">SYNTAX</span></span>

### <span data-ttu-id="7f62e-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7f62e-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f62e-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7f62e-106">GetByResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f62e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f62e-107">DESCRIPTION</span></span>
<span data-ttu-id="7f62e-108">Il cmdlet **Get-AzureRmActivityLogAlert** ottiene una o più risorse di avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="7f62e-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="7f62e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f62e-109">EXAMPLES</span></span>

### <span data-ttu-id="7f62e-110">Esempio 1: ottenere avvisi del log attività tramite ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="7f62e-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="7f62e-111">Questo comando elenca tutti gli avvisi del log attività per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="7f62e-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="7f62e-112">Esempio 2: ottenere avvisi del log attività per il gruppo di risorse specifico</span><span class="sxs-lookup"><span data-stu-id="7f62e-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="7f62e-113">Questo comando elenca gli avvisi del log attività per il gruppo di risorse specifico.</span><span class="sxs-lookup"><span data-stu-id="7f62e-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="7f62e-114">Esempio 3: ottenere un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="7f62e-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="7f62e-115">Questo comando elenca uno (un elenco con un singolo elemento) Avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="7f62e-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="7f62e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f62e-116">PARAMETERS</span></span>

### <span data-ttu-id="7f62e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f62e-117">-DefaultProfile</span></span>
<span data-ttu-id="7f62e-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7f62e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f62e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f62e-119">-Name</span></span>
<span data-ttu-id="7f62e-120">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="7f62e-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="7f62e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f62e-121">-ResourceGroupName</span></span>
<span data-ttu-id="7f62e-122">Nome del gruppo di risorse in cui è presente la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="7f62e-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="7f62e-123">Se nome non è null o vuoto, questo parametro deve contenere una stringa non vuota.</span><span class="sxs-lookup"><span data-stu-id="7f62e-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="7f62e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f62e-124">CommonParameters</span></span>
<span data-ttu-id="7f62e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f62e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f62e-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f62e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f62e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f62e-127">INPUTS</span></span>

### <span data-ttu-id="7f62e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7f62e-128">System.String</span></span>

## <span data-ttu-id="7f62e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f62e-129">OUTPUTS</span></span>

### <span data-ttu-id="7f62e-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="7f62e-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="7f62e-131">Note</span><span class="sxs-lookup"><span data-stu-id="7f62e-131">NOTES</span></span>

## <span data-ttu-id="7f62e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f62e-132">RELATED LINKS</span></span>

[<span data-ttu-id="7f62e-133">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f62e-133">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="7f62e-134">Update-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f62e-134">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="7f62e-135">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f62e-135">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="7f62e-136">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="7f62e-136">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="7f62e-137">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="7f62e-137">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
