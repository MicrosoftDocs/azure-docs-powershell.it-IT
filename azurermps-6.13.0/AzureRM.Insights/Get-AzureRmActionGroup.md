---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
ms.openlocfilehash: 002847ae580e3e3c5d5b44e05ebc1633e4e1574b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686185"
---
# <span data-ttu-id="c0f85-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="c0f85-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="c0f85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0f85-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f85-103">Ottiene i gruppi di azioni.</span><span class="sxs-lookup"><span data-stu-id="c0f85-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0f85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0f85-104">SYNTAX</span></span>

### <span data-ttu-id="c0f85-105">BySubscriptionOrResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c0f85-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0f85-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c0f85-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0f85-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0f85-107">DESCRIPTION</span></span>
<span data-ttu-id="c0f85-108">Il cmdlet **Get-AzureRmActionGroup** ottiene uno o più gruppi di azioni.</span><span class="sxs-lookup"><span data-stu-id="c0f85-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="c0f85-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0f85-109">EXAMPLES</span></span>

### <span data-ttu-id="c0f85-110">Esempio 1: ottenere un gruppo di azioni in base all'ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="c0f85-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="c0f85-111">Questo comando elenca tutti i gruppi di azioni per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="c0f85-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="c0f85-112">Esempio 2: ottenere gruppi di azioni per il gruppo di risorse specifico</span><span class="sxs-lookup"><span data-stu-id="c0f85-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="c0f85-113">Questo comando elenca i gruppi di azioni per il gruppo di risorse specifico.</span><span class="sxs-lookup"><span data-stu-id="c0f85-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="c0f85-114">Esempio 3: ottenere un gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="c0f85-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="c0f85-115">Questo comando elenca uno (un elenco con un singolo elemento) gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="c0f85-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="c0f85-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0f85-116">PARAMETERS</span></span>

### <span data-ttu-id="c0f85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f85-117">-DefaultProfile</span></span>
<span data-ttu-id="c0f85-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c0f85-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0f85-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0f85-119">-Name</span></span>
<span data-ttu-id="c0f85-120">Nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="c0f85-120">The name of the action group.</span></span>

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

### <span data-ttu-id="c0f85-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0f85-121">-ResourceGroupName</span></span>
<span data-ttu-id="c0f85-122">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c0f85-122">The resource group name</span></span>

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

### <span data-ttu-id="c0f85-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f85-123">CommonParameters</span></span>
<span data-ttu-id="c0f85-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0f85-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f85-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0f85-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f85-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0f85-126">INPUTS</span></span>

### <span data-ttu-id="c0f85-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c0f85-127">System.String</span></span>

## <span data-ttu-id="c0f85-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0f85-128">OUTPUTS</span></span>

### <span data-ttu-id="c0f85-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="c0f85-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="c0f85-130">Note</span><span class="sxs-lookup"><span data-stu-id="c0f85-130">NOTES</span></span>

## <span data-ttu-id="c0f85-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0f85-131">RELATED LINKS</span></span>

<span data-ttu-id="c0f85-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="c0f85-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
