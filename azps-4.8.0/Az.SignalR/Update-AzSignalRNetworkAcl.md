---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033726"
---
# <span data-ttu-id="5f146-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="5f146-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="5f146-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f146-102">SYNOPSIS</span></span>
<span data-ttu-id="5f146-103">Aggiornare l'ACL di rete di un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="5f146-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="5f146-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f146-104">SYNTAX</span></span>

### <span data-ttu-id="5f146-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5f146-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f146-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f146-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f146-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f146-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f146-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f146-108">DESCRIPTION</span></span>
<span data-ttu-id="5f146-109">Aggiornare l'ACL di rete di un servizio SignalR, inclusi l'azione predefinita e gli ACL di rete per la connessione pubblica e privata.</span><span class="sxs-lookup"><span data-stu-id="5f146-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="5f146-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f146-110">EXAMPLES</span></span>

### <span data-ttu-id="5f146-111">Consenti RESTAPI, ClientConnection per la rete pubblica e imposta l'azione predefinita su Deny</span><span class="sxs-lookup"><span data-stu-id="5f146-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -DefaultAction Deny -PublicNetwork -Allow RESTAPI,ClientConnection

PS C:\>  $networkAcl

DefaultAction PublicNetwork                                        PrivateEndpoints
------------- -------------                                        ----------------
Deny          Microsoft.Azure.Commands.SignalR.Models.PSNetworkAcl {pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1}

PS C:\> $networkAcl.PublicNetwork
Allow                       Deny
-----                       ----
{ClientConnection, RESTAPI} {}
```

### <span data-ttu-id="5f146-112">Consenti connessione client e connessione al server per una connessione di endpoint privato</span><span class="sxs-lookup"><span data-stu-id="5f146-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="5f146-113">Negare la connessione client sia per la rete pubblica che per una connessione endpoint privata</span><span class="sxs-lookup"><span data-stu-id="5f146-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="5f146-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f146-114">PARAMETERS</span></span>

### <span data-ttu-id="5f146-115">-Consenti</span><span class="sxs-lookup"><span data-stu-id="5f146-115">-Allow</span></span>
<span data-ttu-id="5f146-116">ACL di rete consentiti</span><span class="sxs-lookup"><span data-stu-id="5f146-116">Allowed network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f146-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f146-117">-AsJob</span></span>
<span data-ttu-id="5f146-118">Eseguire il cmdlet in un processo in background.</span><span class="sxs-lookup"><span data-stu-id="5f146-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="5f146-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="5f146-119">-DefaultAction</span></span>
<span data-ttu-id="5f146-120">Azione predefinita degli ACL della rete del segnalatore, Consenti o nega.</span><span class="sxs-lookup"><span data-stu-id="5f146-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="5f146-121">Decide se negare gli ACL di rete o consentire l'effetto ACL della rete.</span><span class="sxs-lookup"><span data-stu-id="5f146-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="5f146-122">Ad esempio, se l'azione predefinita è Allow, solo gli ACL di Deny sono importanti.</span><span class="sxs-lookup"><span data-stu-id="5f146-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f146-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f146-123">-DefaultProfile</span></span>
<span data-ttu-id="5f146-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f146-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f146-125">-Deny</span><span class="sxs-lookup"><span data-stu-id="5f146-125">-Deny</span></span>
<span data-ttu-id="5f146-126">ACL della rete negata</span><span class="sxs-lookup"><span data-stu-id="5f146-126">Denied network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f146-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f146-127">-InputObject</span></span>
<span data-ttu-id="5f146-128">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="5f146-128">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f146-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f146-129">-Name</span></span>
<span data-ttu-id="5f146-130">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="5f146-130">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f146-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="5f146-131">-PrivateEndpointName</span></span>
<span data-ttu-id="5f146-132">Nome/i degli endpoint privati da aggiornare</span><span class="sxs-lookup"><span data-stu-id="5f146-132">Name(s) of private endpoint(s) to be updated</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f146-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="5f146-133">-PublicNetwork</span></span>
<span data-ttu-id="5f146-134">Aggiornare gli elenchi ACL di rete pubblica</span><span class="sxs-lookup"><span data-stu-id="5f146-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="5f146-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f146-135">-ResourceGroupName</span></span>
<span data-ttu-id="5f146-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5f146-136">The resource group name.</span></span>
<span data-ttu-id="5f146-137">Verrà usato quello predefinito se non specificato.</span><span class="sxs-lookup"><span data-stu-id="5f146-137">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f146-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f146-138">-ResourceId</span></span>
<span data-ttu-id="5f146-139">ID risorsa del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="5f146-139">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f146-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5f146-140">-Confirm</span></span>
<span data-ttu-id="5f146-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f146-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f146-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f146-142">-WhatIf</span></span>
<span data-ttu-id="5f146-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f146-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f146-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f146-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f146-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f146-145">CommonParameters</span></span>
<span data-ttu-id="5f146-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f146-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f146-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f146-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f146-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f146-148">INPUTS</span></span>

### <span data-ttu-id="5f146-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5f146-149">System.String</span></span>

## <span data-ttu-id="5f146-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f146-150">OUTPUTS</span></span>

### <span data-ttu-id="5f146-151">Microsoft. Azure. Commands. SignalR. Models. PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="5f146-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="5f146-152">Note</span><span class="sxs-lookup"><span data-stu-id="5f146-152">NOTES</span></span>

## <span data-ttu-id="5f146-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f146-153">RELATED LINKS</span></span>
