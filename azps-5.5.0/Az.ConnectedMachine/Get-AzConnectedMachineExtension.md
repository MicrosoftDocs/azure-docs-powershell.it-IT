---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209922"
---
# <span data-ttu-id="5d8e1-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="5d8e1-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="5d8e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="5d8e1-103">Operazione per ottenere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="5d8e1-103">The operation to get the extension.</span></span>

## <span data-ttu-id="5d8e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d8e1-104">SYNTAX</span></span>

### <span data-ttu-id="5d8e1-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5d8e1-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5d8e1-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="5d8e1-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5d8e1-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5d8e1-107">DESCRIPTION</span></span>
<span data-ttu-id="5d8e1-108">Operazione per ottenere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="5d8e1-108">The operation to get the extension.</span></span>

## <span data-ttu-id="5d8e1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d8e1-109">EXAMPLES</span></span>

### <span data-ttu-id="5d8e1-110">Esempio 1: Elencare tutte le estensioni per un computer</span><span class="sxs-lookup"><span data-stu-id="5d8e1-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="5d8e1-111">Elenca tutte le estensioni per un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="5d8e1-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="5d8e1-112">Esempio 2: Ottenere un'estensione specifica in un computer</span><span class="sxs-lookup"><span data-stu-id="5d8e1-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="5d8e1-113">Ottiene un'estensione specifica in un computer.</span><span class="sxs-lookup"><span data-stu-id="5d8e1-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="5d8e1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d8e1-114">PARAMETERS</span></span>

### <span data-ttu-id="5d8e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d8e1-115">-DefaultProfile</span></span>
<span data-ttu-id="5d8e1-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d8e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d8e1-117">-Expand</span><span class="sxs-lookup"><span data-stu-id="5d8e1-117">-Expand</span></span>
<span data-ttu-id="5d8e1-118">Espressione di espansione da applicare all'operazione.</span><span class="sxs-lookup"><span data-stu-id="5d8e1-118">The expand expression to apply on the operation.</span></span>

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

### <span data-ttu-id="5d8e1-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="5d8e1-119">-MachineName</span></span>
<span data-ttu-id="5d8e1-120">Nome del computer che contiene l'estensione.</span><span class="sxs-lookup"><span data-stu-id="5d8e1-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="5d8e1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5d8e1-121">-Name</span></span>
<span data-ttu-id="5d8e1-122">Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="5d8e1-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="5d8e1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d8e1-123">-ResourceGroupName</span></span>
<span data-ttu-id="5d8e1-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d8e1-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d8e1-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d8e1-125">-SubscriptionId</span></span>
<span data-ttu-id="5d8e1-126">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5d8e1-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5d8e1-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5d8e1-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5d8e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d8e1-128">CommonParameters</span></span>
<span data-ttu-id="5d8e1-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d8e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d8e1-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d8e1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d8e1-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="5d8e1-131">INPUTS</span></span>

## <span data-ttu-id="5d8e1-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d8e1-132">OUTPUTS</span></span>

### <span data-ttu-id="5d8e1-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="5d8e1-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="5d8e1-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="5d8e1-134">NOTES</span></span>

<span data-ttu-id="5d8e1-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5d8e1-135">ALIASES</span></span>

## <span data-ttu-id="5d8e1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d8e1-136">RELATED LINKS</span></span>

