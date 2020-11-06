---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: 41ed224333d9d0ab1aa542629f46fcf6d8db5fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521436"
---
# <span data-ttu-id="9dbb4-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9dbb4-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="9dbb4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9dbb4-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbb4-103">Ottiene una o più risorse di avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="9dbb4-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dbb4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9dbb4-104">SYNTAX</span></span>

### <span data-ttu-id="9dbb4-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9dbb4-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dbb4-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9dbb4-106">GetByResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9dbb4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9dbb4-107">DESCRIPTION</span></span>
<span data-ttu-id="9dbb4-108">Il cmdlet **Get-AzureRmActivityLogAlert** ottiene una o più risorse di avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="9dbb4-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="9dbb4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9dbb4-109">EXAMPLES</span></span>

### <span data-ttu-id="9dbb4-110">Esempio 1: ottenere avvisi del log attività tramite ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="9dbb4-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="9dbb4-111">Questo comando elenca tutti gli avvisi del log attività per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="9dbb4-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="9dbb4-112">Esempio 2: ottenere avvisi del log attività per il gruppo di risorse specifico</span><span class="sxs-lookup"><span data-stu-id="9dbb4-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="9dbb4-113">Questo comando elenca gli avvisi del log attività per il gruppo di risorse specifico.</span><span class="sxs-lookup"><span data-stu-id="9dbb4-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="9dbb4-114">Esempio 3: ottenere un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="9dbb4-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="9dbb4-115">Questo comando elenca uno (un elenco con un singolo elemento) Avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="9dbb4-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="9dbb4-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9dbb4-116">PARAMETERS</span></span>

### <span data-ttu-id="9dbb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dbb4-117">-DefaultProfile</span></span>
<span data-ttu-id="9dbb4-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9dbb4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dbb4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9dbb4-119">-Name</span></span>
<span data-ttu-id="9dbb4-120">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="9dbb4-120">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dbb4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dbb4-121">-ResourceGroupName</span></span>
<span data-ttu-id="9dbb4-122">Nome del gruppo di risorse in cui è presente la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="9dbb4-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="9dbb4-123">Se nome non è null o vuoto, questo parametro deve contenere una stringa non vuota.</span><span class="sxs-lookup"><span data-stu-id="9dbb4-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dbb4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbb4-124">CommonParameters</span></span>
<span data-ttu-id="9dbb4-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dbb4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbb4-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dbb4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbb4-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9dbb4-127">INPUTS</span></span>

### <span data-ttu-id="9dbb4-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9dbb4-128">None</span></span>

## <span data-ttu-id="9dbb4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9dbb4-129">OUTPUTS</span></span>

### <span data-ttu-id="9dbb4-130"><System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource]</span><span class="sxs-lookup"><span data-stu-id="9dbb4-130"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource]</span></span>

### <span data-ttu-id="9dbb4-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9dbb4-131">None</span></span>

## <span data-ttu-id="9dbb4-132">Note</span><span class="sxs-lookup"><span data-stu-id="9dbb4-132">NOTES</span></span>

## <span data-ttu-id="9dbb4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9dbb4-133">RELATED LINKS</span></span>

[<span data-ttu-id="9dbb4-134">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9dbb4-134">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9dbb4-135">Update-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9dbb4-135">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9dbb4-136">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9dbb4-136">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9dbb4-137">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="9dbb4-137">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="9dbb4-138">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="9dbb4-138">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
