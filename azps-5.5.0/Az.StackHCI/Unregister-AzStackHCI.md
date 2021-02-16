---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e5ff59889b2b786d07699a5b9d46937372c0662f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176663"
---
# <span data-ttu-id="b2598-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="b2598-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="b2598-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2598-102">SYNOPSIS</span></span>
<span data-ttu-id="b2598-103">Unregister-AzStackHCI elimina la risorsa cloud Microsoft.AzureStackHCI che rappresenta il cluster locale e annulla la registrazione del cluster locale con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2598-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="b2598-104">Le informazioni registrate disponibili nel cluster vengono usate per annullare la registrazione del cluster se non vengono passati parametri.</span><span class="sxs-lookup"><span data-stu-id="b2598-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="b2598-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2598-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2598-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b2598-106">DESCRIPTION</span></span>
<span data-ttu-id="b2598-107">Unregister-AzStackHCI elimina la risorsa cloud Microsoft.AzureStackHCI che rappresenta il cluster locale e annulla la registrazione del cluster locale con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2598-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="b2598-108">Le informazioni registrate disponibili nel cluster vengono usate per annullare la registrazione del cluster se non vengono passati parametri.</span><span class="sxs-lookup"><span data-stu-id="b2598-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="b2598-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2598-109">EXAMPLES</span></span>

### <span data-ttu-id="b2598-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="b2598-110">EXAMPLE 1</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI
Result: Success
```
<span data-ttu-id="b2598-111">Richiamo in uno dei nodi del cluster</span><span class="sxs-lookup"><span data-stu-id="b2598-111">Invoking on one of the cluster node</span></span>

### <span data-ttu-id="b2598-112">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="b2598-112">EXAMPLE 2</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1
Result: Success
```
<span data-ttu-id="b2598-113">Richiamo dal nodo di gestione</span><span class="sxs-lookup"><span data-stu-id="b2598-113">Invoking from the management node</span></span>

### <span data-ttu-id="b2598-114">ESEMPIO 3</span><span class="sxs-lookup"><span data-stu-id="b2598-114">EXAMPLE 3</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False
Result: Success
```
<span data-ttu-id="b2598-115">Richiamo da WAC</span><span class="sxs-lookup"><span data-stu-id="b2598-115">Invoking from WAC</span></span>

### <span data-ttu-id="b2598-116">ESEMPIO 4</span><span class="sxs-lookup"><span data-stu-id="b2598-116">EXAMPLE 4</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
```
<span data-ttu-id="b2598-117">Richiamo con tutti i parametri</span><span class="sxs-lookup"><span data-stu-id="b2598-117">Invoking with all the parameters</span></span>

## <span data-ttu-id="b2598-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2598-118">PARAMETERS</span></span>

### <span data-ttu-id="b2598-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="b2598-119">-AccountId</span></span>
<span data-ttu-id="b2598-120">Specifica il token ARM di accesso rapido.</span><span class="sxs-lookup"><span data-stu-id="b2598-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="b2598-121">Se si specifica questa opzione insieme a ArmAccessToken e GraphAccessToken, si evita l'accesso interattivo di Azure.</span><span class="sxs-lookup"><span data-stu-id="b2598-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2598-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="b2598-122">-ArmAccessToken</span></span>
<span data-ttu-id="b2598-123">Specifica il token ARM di accesso rapido.</span><span class="sxs-lookup"><span data-stu-id="b2598-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="b2598-124">Se si specifica questa opzione insieme a GraphAccessToken e AccountId, si evita l'accesso interattivo ad Azure.</span><span class="sxs-lookup"><span data-stu-id="b2598-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2598-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="b2598-125">-ComputerName</span></span>
<span data-ttu-id="b2598-126">Specifica uno del nodo del cluster nel cluster locale che viene registrato in Azure.</span><span class="sxs-lookup"><span data-stu-id="b2598-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2598-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="b2598-127">-Credential</span></span>
<span data-ttu-id="b2598-128">Specifica le credenziali per NomeComputer.</span><span class="sxs-lookup"><span data-stu-id="b2598-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="b2598-129">Il valore predefinito è l'utente corrente che esegue il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2598-129">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2598-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="b2598-130">-EnvironmentName</span></span>
<span data-ttu-id="b2598-131">Specifica l'ambiente di Azure.</span><span class="sxs-lookup"><span data-stu-id="b2598-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="b2598-132">Il valore predefinito è AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="b2598-132">Default is AzureCloud.</span></span>
<span data-ttu-id="b2598-133">I valori validi sono AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="b2598-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2598-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="b2598-134">-GraphAccessToken</span></span>
<span data-ttu-id="b2598-135">Specifica il token di accesso Graph.</span><span class="sxs-lookup"><span data-stu-id="b2598-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="b2598-136">Se si specifica questa opzione insieme a ArmAccessToken e AccountId, si evita l'accesso interattivo ad Azure.</span><span class="sxs-lookup"><span data-stu-id="b2598-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2598-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2598-137">-ResourceGroupName</span></span>
<span data-ttu-id="b2598-138">Specifica il nome del gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="b2598-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="b2598-139">Se non si \<LocalClusterName\> è specificato -rg, verrà usato come nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2598-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2598-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b2598-140">-ResourceName</span></span>
<span data-ttu-id="b2598-141">Specifica il nome della risorsa creata in Azure.</span><span class="sxs-lookup"><span data-stu-id="b2598-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="b2598-142">Se non viene specificato, viene usato il nome del cluster locale.</span><span class="sxs-lookup"><span data-stu-id="b2598-142">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2598-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2598-143">-SubscriptionId</span></span>
<span data-ttu-id="b2598-144">Specifica la sottoscrizione di Azure per creare la risorsa</span><span class="sxs-lookup"><span data-stu-id="b2598-144">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2598-145">-TenantId</span><span class="sxs-lookup"><span data-stu-id="b2598-145">-TenantId</span></span>
<span data-ttu-id="b2598-146">Specifica il valore di Azure TenantId.</span><span class="sxs-lookup"><span data-stu-id="b2598-146">Specifies the Azure TenantId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2598-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="b2598-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="b2598-148">Usa l'autenticazione del codice del dispositivo invece di una richiesta interattiva del browser.</span><span class="sxs-lookup"><span data-stu-id="b2598-148">Use device code authentication instead of an interactive browser prompt.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2598-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2598-149">-Confirm</span></span>
<span data-ttu-id="b2598-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2598-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2598-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2598-151">-WhatIf</span></span>
<span data-ttu-id="b2598-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2598-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2598-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2598-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2598-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2598-154">CommonParameters</span></span>
<span data-ttu-id="b2598-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2598-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2598-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b2598-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2598-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="b2598-157">INPUTS</span></span>

## <span data-ttu-id="b2598-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2598-158">OUTPUTS</span></span>

### <span data-ttu-id="b2598-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="b2598-159">PSCustomObject.</span></span> <span data-ttu-id="b2598-160">Restituisce le proprietà seguenti in PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="b2598-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="b2598-161">Risultato: Operazione riuscita o Non riuscita o Annullata.</span><span class="sxs-lookup"><span data-stu-id="b2598-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="b2598-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="b2598-162">NOTES</span></span>

## <span data-ttu-id="b2598-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2598-163">RELATED LINKS</span></span>
