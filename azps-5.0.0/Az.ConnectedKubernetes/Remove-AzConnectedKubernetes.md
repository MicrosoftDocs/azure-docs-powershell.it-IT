---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200213"
---
# <span data-ttu-id="6d1a8-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="6d1a8-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="6d1a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d1a8-102">SYNOPSIS</span></span>
<span data-ttu-id="6d1a8-103">Eliminare un cluster connesso, rimuovendo la risorsa rilevata in Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="6d1a8-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="6d1a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d1a8-104">SYNTAX</span></span>

### <span data-ttu-id="6d1a8-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d1a8-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d1a8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6d1a8-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6d1a8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d1a8-107">DESCRIPTION</span></span>
<span data-ttu-id="6d1a8-108">Eliminare un cluster connesso, rimuovendo la risorsa rilevata in Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="6d1a8-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="6d1a8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d1a8-109">EXAMPLES</span></span>

### <span data-ttu-id="6d1a8-110">Esempio 1: rimuovere un kubernetes connesso</span><span class="sxs-lookup"><span data-stu-id="6d1a8-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="6d1a8-111">Questo comando rimuove un kubernetes connesso</span><span class="sxs-lookup"><span data-stu-id="6d1a8-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="6d1a8-112">Esempio 2: rimuovere un kubernetes connesso per oggetto</span><span class="sxs-lookup"><span data-stu-id="6d1a8-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="6d1a8-113">Questo comando rimuove un oggetto kubernetes connesso</span><span class="sxs-lookup"><span data-stu-id="6d1a8-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="6d1a8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d1a8-114">PARAMETERS</span></span>

### <span data-ttu-id="6d1a8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d1a8-115">-AsJob</span></span>
<span data-ttu-id="6d1a8-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="6d1a8-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a8-117">-Clustername</span><span class="sxs-lookup"><span data-stu-id="6d1a8-117">-ClusterName</span></span>
<span data-ttu-id="6d1a8-118">Nome del cluster Kubernetes in cui viene chiamato Get.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-118">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d1a8-119">-DefaultProfile</span></span>
<span data-ttu-id="6d1a8-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d1a8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d1a8-121">-InputObject</span></span>
<span data-ttu-id="6d1a8-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a8-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="6d1a8-123">-KubeConfig</span></span>
<span data-ttu-id="6d1a8-124">Percorso del file di configurazione Kube</span><span class="sxs-lookup"><span data-stu-id="6d1a8-124">Path to the kube config file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a8-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="6d1a8-125">-KubeContext</span></span>
<span data-ttu-id="6d1a8-126">Contesto Kubconfig dal computer corrente</span><span class="sxs-lookup"><span data-stu-id="6d1a8-126">Kubconfig context from current machine</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a8-127">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="6d1a8-127">-NoWait</span></span>
<span data-ttu-id="6d1a8-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="6d1a8-128">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d1a8-129">-PassThru</span></span>
<span data-ttu-id="6d1a8-130">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="6d1a8-130">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d1a8-131">-ResourceGroupName</span></span>
<span data-ttu-id="6d1a8-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-132">The name of the resource group.</span></span>
<span data-ttu-id="6d1a8-133">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-133">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a8-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d1a8-134">-SubscriptionId</span></span>
<span data-ttu-id="6d1a8-135">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a8-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6d1a8-136">-Confirm</span></span>
<span data-ttu-id="6d1a8-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d1a8-138">-WhatIf</span></span>
<span data-ttu-id="6d1a8-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d1a8-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d1a8-141">CommonParameters</span></span>
<span data-ttu-id="6d1a8-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d1a8-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d1a8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d1a8-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d1a8-144">INPUTS</span></span>

### <span data-ttu-id="6d1a8-145">Microsoft. Azure. PowerShell. Cmdlets. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="6d1a8-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="6d1a8-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d1a8-146">OUTPUTS</span></span>

### <span data-ttu-id="6d1a8-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d1a8-147">System.Boolean</span></span>

## <span data-ttu-id="6d1a8-148">Note</span><span class="sxs-lookup"><span data-stu-id="6d1a8-148">NOTES</span></span>

<span data-ttu-id="6d1a8-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6d1a8-149">ALIASES</span></span>

<span data-ttu-id="6d1a8-150">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d1a8-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d1a8-151">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d1a8-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d1a8-153">INPUTOBJECT <IConnectedKubernetesIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="6d1a8-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d1a8-154">`[ClusterName <String>]`: Nome del cluster Kubernetes in cui viene chiamato Get.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="6d1a8-155">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="6d1a8-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d1a8-156">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6d1a8-157">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="6d1a8-158">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6d1a8-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="6d1a8-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d1a8-159">RELATED LINKS</span></span>

