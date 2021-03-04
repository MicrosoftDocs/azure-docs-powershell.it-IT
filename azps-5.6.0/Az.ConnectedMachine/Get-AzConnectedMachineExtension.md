---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: 423834d0dc7a324743795e0d54324a51f1cd04ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012398"
---
# <span data-ttu-id="3de33-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="3de33-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="3de33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3de33-102">SYNOPSIS</span></span>
<span data-ttu-id="3de33-103">Operazione per ottenere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="3de33-103">The operation to get the extension.</span></span>

## <span data-ttu-id="3de33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3de33-104">SYNTAX</span></span>

### <span data-ttu-id="3de33-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3de33-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3de33-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="3de33-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3de33-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3de33-107">DESCRIPTION</span></span>
<span data-ttu-id="3de33-108">Operazione per ottenere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="3de33-108">The operation to get the extension.</span></span>

## <span data-ttu-id="3de33-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3de33-109">EXAMPLES</span></span>

### <span data-ttu-id="3de33-110">Esempio 1: Elencare tutte le estensioni per un computer</span><span class="sxs-lookup"><span data-stu-id="3de33-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="3de33-111">Elenca tutte le estensioni per un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="3de33-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="3de33-112">Esempio 2: Ottenere un'estensione specifica in un computer</span><span class="sxs-lookup"><span data-stu-id="3de33-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="3de33-113">Ottiene un'estensione specifica in un computer.</span><span class="sxs-lookup"><span data-stu-id="3de33-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="3de33-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3de33-114">PARAMETERS</span></span>

### <span data-ttu-id="3de33-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de33-115">-DefaultProfile</span></span>
<span data-ttu-id="3de33-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3de33-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de33-117">-Expand</span><span class="sxs-lookup"><span data-stu-id="3de33-117">-Expand</span></span>
<span data-ttu-id="3de33-118">Espressione di espansione da applicare all'operazione.</span><span class="sxs-lookup"><span data-stu-id="3de33-118">The expand expression to apply on the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de33-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="3de33-119">-MachineName</span></span>
<span data-ttu-id="3de33-120">Nome del computer che contiene l'estensione.</span><span class="sxs-lookup"><span data-stu-id="3de33-120">The name of the machine containing the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de33-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3de33-121">-Name</span></span>
<span data-ttu-id="3de33-122">Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="3de33-122">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de33-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3de33-123">-ResourceGroupName</span></span>
<span data-ttu-id="3de33-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3de33-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de33-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3de33-125">-SubscriptionId</span></span>
<span data-ttu-id="3de33-126">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3de33-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3de33-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3de33-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de33-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de33-128">CommonParameters</span></span>
<span data-ttu-id="3de33-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3de33-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de33-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3de33-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de33-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="3de33-131">INPUTS</span></span>

## <span data-ttu-id="3de33-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3de33-132">OUTPUTS</span></span>

### <span data-ttu-id="3de33-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="3de33-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="3de33-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="3de33-134">NOTES</span></span>

<span data-ttu-id="3de33-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3de33-135">ALIASES</span></span>

## <span data-ttu-id="3de33-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3de33-136">RELATED LINKS</span></span>

