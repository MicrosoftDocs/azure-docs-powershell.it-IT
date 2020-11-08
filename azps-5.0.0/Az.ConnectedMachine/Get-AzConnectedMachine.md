---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: afb6a5bab6c2761095fb3ab69a2898aeeb53b45c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202203"
---
# <span data-ttu-id="0bb1c-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="0bb1c-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="0bb1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0bb1c-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb1c-103">Recupera le informazioni sulla visualizzazione modello o la visualizzazione istanza di una macchina ibrida.</span><span class="sxs-lookup"><span data-stu-id="0bb1c-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="0bb1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bb1c-104">SYNTAX</span></span>

### <span data-ttu-id="0bb1c-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0bb1c-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0bb1c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="0bb1c-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0bb1c-107">Elenco</span><span class="sxs-lookup"><span data-stu-id="0bb1c-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0bb1c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bb1c-108">DESCRIPTION</span></span>
<span data-ttu-id="0bb1c-109">Recupera le informazioni sulla visualizzazione modello o la visualizzazione istanza di una macchina ibrida.</span><span class="sxs-lookup"><span data-stu-id="0bb1c-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="0bb1c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bb1c-110">EXAMPLES</span></span>

### <span data-ttu-id="0bb1c-111">Esempio 1: elencare tutti i computer connessi in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="0bb1c-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="0bb1c-112">Elenca tutti i computer connessi in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0bb1c-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="0bb1c-113">Se l'abbonamento non viene specificato, utilizzerà l'abbonamento dal contesto corrente di PowerShell di Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb1c-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="0bb1c-114">Esempio 2: elencare tutti i computer connessi in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0bb1c-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="0bb1c-115">Elencare tutti i computer connessi in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0bb1c-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="0bb1c-116">Esempio 3: ottenere un computer connesso in un gruppo di risorse per nome</span><span class="sxs-lookup"><span data-stu-id="0bb1c-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="0bb1c-117">Ottenere un computer connesso in un gruppo di risorse per nome.</span><span class="sxs-lookup"><span data-stu-id="0bb1c-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="0bb1c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0bb1c-118">PARAMETERS</span></span>

### <span data-ttu-id="0bb1c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb1c-119">-DefaultProfile</span></span>
<span data-ttu-id="0bb1c-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb1c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bb1c-121">-Espandi</span><span class="sxs-lookup"><span data-stu-id="0bb1c-121">-Expand</span></span>
<span data-ttu-id="0bb1c-122">Espressione expand da applicare all'operazione.</span><span class="sxs-lookup"><span data-stu-id="0bb1c-122">The expand expression to apply on the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Support.InstanceViewTypes
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb1c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0bb1c-123">-Name</span></span>
<span data-ttu-id="0bb1c-124">Nome della macchina ibrida.</span><span class="sxs-lookup"><span data-stu-id="0bb1c-124">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="0bb1c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bb1c-125">-ResourceGroupName</span></span>
<span data-ttu-id="0bb1c-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0bb1c-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb1c-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0bb1c-127">-SubscriptionId</span></span>
<span data-ttu-id="0bb1c-128">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb1c-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0bb1c-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0bb1c-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0bb1c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb1c-130">CommonParameters</span></span>
<span data-ttu-id="0bb1c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bb1c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb1c-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bb1c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb1c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0bb1c-133">INPUTS</span></span>

## <span data-ttu-id="0bb1c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bb1c-134">OUTPUTS</span></span>

### <span data-ttu-id="0bb1c-135">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachine</span><span class="sxs-lookup"><span data-stu-id="0bb1c-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="0bb1c-136">Note</span><span class="sxs-lookup"><span data-stu-id="0bb1c-136">NOTES</span></span>

<span data-ttu-id="0bb1c-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0bb1c-137">ALIASES</span></span>

## <span data-ttu-id="0bb1c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bb1c-138">RELATED LINKS</span></span>

