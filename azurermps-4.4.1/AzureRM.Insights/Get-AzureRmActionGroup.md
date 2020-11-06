---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
ms.openlocfilehash: 4edb403452d262705fe8fa61691ac77ba4524977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521632"
---
# <span data-ttu-id="a7e2e-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a7e2e-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="a7e2e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e2e-103">Ottiene i gruppi di azioni.</span><span class="sxs-lookup"><span data-stu-id="a7e2e-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7e2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7e2e-104">SYNTAX</span></span>

### <span data-ttu-id="a7e2e-105">BySubscriptionOrResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a7e2e-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7e2e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a7e2e-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7e2e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7e2e-107">DESCRIPTION</span></span>
<span data-ttu-id="a7e2e-108">Il cmdlet **Get-AzureRmActionGroup** ottiene uno o più gruppi di azioni.</span><span class="sxs-lookup"><span data-stu-id="a7e2e-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="a7e2e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7e2e-109">EXAMPLES</span></span>

### <span data-ttu-id="a7e2e-110">Esempio 1: ottenere un gruppo di azioni in base all'ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="a7e2e-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="a7e2e-111">Questo comando elenca tutti i gruppi di azioni per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="a7e2e-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="a7e2e-112">Esempio 2: ottenere gruppi di azioni per il gruppo di risorse specifico</span><span class="sxs-lookup"><span data-stu-id="a7e2e-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="a7e2e-113">Questo comando elenca i gruppi di azioni per il gruppo di risorse specifico.</span><span class="sxs-lookup"><span data-stu-id="a7e2e-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="a7e2e-114">Esempio 3: ottenere un gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="a7e2e-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="a7e2e-115">Questo comando elenca uno (un elenco con un singolo elemento) gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="a7e2e-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="a7e2e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7e2e-116">PARAMETERS</span></span>

### <span data-ttu-id="a7e2e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7e2e-117">-Name</span></span>
<span data-ttu-id="a7e2e-118">Nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="a7e2e-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7e2e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e2e-119">-DefaultProfile</span></span>
<span data-ttu-id="a7e2e-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e2e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7e2e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7e2e-121">-ResourceGroupName</span></span>
<span data-ttu-id="a7e2e-122">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a7e2e-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7e2e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e2e-123">CommonParameters</span></span>
<span data-ttu-id="a7e2e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7e2e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e2e-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7e2e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e2e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7e2e-126">INPUTS</span></span>

### <span data-ttu-id="a7e2e-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a7e2e-127">None</span></span>

## <span data-ttu-id="a7e2e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7e2e-128">OUTPUTS</span></span>

### <span data-ttu-id="a7e2e-129"><System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource]</span><span class="sxs-lookup"><span data-stu-id="a7e2e-129"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource]</span></span>

### <span data-ttu-id="a7e2e-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a7e2e-130">None</span></span>

## <span data-ttu-id="a7e2e-131">Note</span><span class="sxs-lookup"><span data-stu-id="a7e2e-131">NOTES</span></span>

## <span data-ttu-id="a7e2e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7e2e-132">RELATED LINKS</span></span>

<span data-ttu-id="a7e2e-133">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="a7e2e-133">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
