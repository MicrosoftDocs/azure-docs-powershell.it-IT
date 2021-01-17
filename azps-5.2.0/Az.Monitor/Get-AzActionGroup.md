---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: 90bd9c7943e6e788d81f8ddec85513676afade23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365326"
---
# <span data-ttu-id="b3b84-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="b3b84-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="b3b84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3b84-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b84-103">Ottiene i gruppi di azioni.</span><span class="sxs-lookup"><span data-stu-id="b3b84-103">Gets action group(s).</span></span>

## <span data-ttu-id="b3b84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3b84-104">SYNTAX</span></span>

### <span data-ttu-id="b3b84-105">BySubscriptionOrResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3b84-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b84-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b3b84-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3b84-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3b84-107">DESCRIPTION</span></span>
<span data-ttu-id="b3b84-108">Il cmdlet **Get-AzActionGroup** ottiene uno o più gruppi di azioni.</span><span class="sxs-lookup"><span data-stu-id="b3b84-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="b3b84-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3b84-109">EXAMPLES</span></span>

### <span data-ttu-id="b3b84-110">Esempio 1: ottenere un gruppo di azioni in base all'ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="b3b84-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="b3b84-111">Questo comando elenca tutti i gruppi di azioni per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b3b84-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="b3b84-112">Esempio 2: ottenere gruppi di azioni per il gruppo di risorse specifico</span><span class="sxs-lookup"><span data-stu-id="b3b84-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="b3b84-113">Questo comando elenca i gruppi di azioni per il gruppo di risorse specifico.</span><span class="sxs-lookup"><span data-stu-id="b3b84-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="b3b84-114">Esempio 3: ottenere un gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="b3b84-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="b3b84-115">Questo comando elenca uno (un elenco con un singolo elemento) gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="b3b84-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="b3b84-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3b84-116">PARAMETERS</span></span>

### <span data-ttu-id="b3b84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b84-117">-DefaultProfile</span></span>
<span data-ttu-id="b3b84-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b3b84-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3b84-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3b84-119">-Name</span></span>
<span data-ttu-id="b3b84-120">Nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="b3b84-120">The name of the action group.</span></span>

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

### <span data-ttu-id="b3b84-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3b84-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3b84-122">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b3b84-122">The resource group name</span></span>

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

### <span data-ttu-id="b3b84-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b84-123">CommonParameters</span></span>
<span data-ttu-id="b3b84-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b84-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b84-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3b84-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b84-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3b84-126">INPUTS</span></span>

### <span data-ttu-id="b3b84-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b3b84-127">System.String</span></span>

## <span data-ttu-id="b3b84-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3b84-128">OUTPUTS</span></span>

### <span data-ttu-id="b3b84-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="b3b84-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="b3b84-130">Note</span><span class="sxs-lookup"><span data-stu-id="b3b84-130">NOTES</span></span>

## <span data-ttu-id="b3b84-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3b84-131">RELATED LINKS</span></span>

<span data-ttu-id="b3b84-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="b3b84-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
