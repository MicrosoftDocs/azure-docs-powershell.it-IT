---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191349"
---
# <span data-ttu-id="97526-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="97526-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="97526-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97526-102">SYNOPSIS</span></span>
<span data-ttu-id="97526-103">Operazione per ottenere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="97526-103">The operation to get the extension.</span></span>

## <span data-ttu-id="97526-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97526-104">SYNTAX</span></span>

### <span data-ttu-id="97526-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97526-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="97526-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="97526-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="97526-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97526-107">DESCRIPTION</span></span>
<span data-ttu-id="97526-108">Operazione per ottenere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="97526-108">The operation to get the extension.</span></span>

## <span data-ttu-id="97526-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97526-109">EXAMPLES</span></span>

### <span data-ttu-id="97526-110">Esempio 1: elencare tutte le estensioni per un computer</span><span class="sxs-lookup"><span data-stu-id="97526-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="97526-111">Elenca tutte le estensioni per un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="97526-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="97526-112">Esempio 2: ottenere un'estensione specifica in un computer</span><span class="sxs-lookup"><span data-stu-id="97526-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="97526-113">Ottiene un'estensione specifica in un computer.</span><span class="sxs-lookup"><span data-stu-id="97526-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="97526-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97526-114">PARAMETERS</span></span>

### <span data-ttu-id="97526-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97526-115">-DefaultProfile</span></span>
<span data-ttu-id="97526-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97526-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97526-117">-Espandi</span><span class="sxs-lookup"><span data-stu-id="97526-117">-Expand</span></span>
<span data-ttu-id="97526-118">Espressione expand da applicare all'operazione.</span><span class="sxs-lookup"><span data-stu-id="97526-118">The expand expression to apply on the operation.</span></span>

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

### <span data-ttu-id="97526-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="97526-119">-MachineName</span></span>
<span data-ttu-id="97526-120">Il nome del computer che contiene l'estensione.</span><span class="sxs-lookup"><span data-stu-id="97526-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="97526-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="97526-121">-Name</span></span>
<span data-ttu-id="97526-122">Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="97526-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="97526-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97526-123">-ResourceGroupName</span></span>
<span data-ttu-id="97526-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="97526-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="97526-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97526-125">-SubscriptionId</span></span>
<span data-ttu-id="97526-126">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="97526-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="97526-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="97526-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="97526-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97526-128">CommonParameters</span></span>
<span data-ttu-id="97526-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97526-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97526-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97526-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97526-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97526-131">INPUTS</span></span>

## <span data-ttu-id="97526-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97526-132">OUTPUTS</span></span>

### <span data-ttu-id="97526-133">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="97526-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="97526-134">Note</span><span class="sxs-lookup"><span data-stu-id="97526-134">NOTES</span></span>

<span data-ttu-id="97526-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="97526-135">ALIASES</span></span>

## <span data-ttu-id="97526-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97526-136">RELATED LINKS</span></span>

