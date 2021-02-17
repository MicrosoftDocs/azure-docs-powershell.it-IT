---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207994"
---
# <span data-ttu-id="20ae1-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="20ae1-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="20ae1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="20ae1-103">Aggiornare l'ACL di rete di un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="20ae1-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="20ae1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20ae1-104">SYNTAX</span></span>

### <span data-ttu-id="20ae1-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="20ae1-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20ae1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20ae1-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20ae1-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20ae1-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20ae1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="20ae1-108">DESCRIPTION</span></span>
<span data-ttu-id="20ae1-109">Aggiorna l'ACL di rete di un servizio SignalR, incluse l'azione predefinita e gli ACL di rete per la connessione pubblica e privata.</span><span class="sxs-lookup"><span data-stu-id="20ae1-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="20ae1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20ae1-110">EXAMPLES</span></span>

### <span data-ttu-id="20ae1-111">Consentire RESTAPI,ClientConnection per la rete pubblica e impostare l'azione predefinita su Nega</span><span class="sxs-lookup"><span data-stu-id="20ae1-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
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

### <span data-ttu-id="20ae1-112">Consenti connessione client e connessione server per una connessione all'endpoint privata</span><span class="sxs-lookup"><span data-stu-id="20ae1-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="20ae1-113">Nega connessione client sia per la rete pubblica che per una connessione all'endpoint privato</span><span class="sxs-lookup"><span data-stu-id="20ae1-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="20ae1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20ae1-114">PARAMETERS</span></span>

### <span data-ttu-id="20ae1-115">-Allow</span><span class="sxs-lookup"><span data-stu-id="20ae1-115">-Allow</span></span>
<span data-ttu-id="20ae1-116">ACL di rete consentiti</span><span class="sxs-lookup"><span data-stu-id="20ae1-116">Allowed network ACLs</span></span>

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

### <span data-ttu-id="20ae1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20ae1-117">-AsJob</span></span>
<span data-ttu-id="20ae1-118">Eseguire il cmdlet in un processo in background.</span><span class="sxs-lookup"><span data-stu-id="20ae1-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="20ae1-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="20ae1-119">-DefaultAction</span></span>
<span data-ttu-id="20ae1-120">Azione predefinita degli ACL di rete SignalR, sia consentiti che negati.</span><span class="sxs-lookup"><span data-stu-id="20ae1-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="20ae1-121">Decide se è necessario rifiutare gli ACL di rete o consentire gli ACL di rete.</span><span class="sxs-lookup"><span data-stu-id="20ae1-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="20ae1-122">Ad esempio, se l'azione predefinita è consentita, hanno importanza solo gli elenchi di controllo di accesso non consentiti.</span><span class="sxs-lookup"><span data-stu-id="20ae1-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

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

### <span data-ttu-id="20ae1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ae1-123">-DefaultProfile</span></span>
<span data-ttu-id="20ae1-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20ae1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20ae1-125">-Nega</span><span class="sxs-lookup"><span data-stu-id="20ae1-125">-Deny</span></span>
<span data-ttu-id="20ae1-126">ACL di rete rifiutati</span><span class="sxs-lookup"><span data-stu-id="20ae1-126">Denied network ACLs</span></span>

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

### <span data-ttu-id="20ae1-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20ae1-127">-InputObject</span></span>
<span data-ttu-id="20ae1-128">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="20ae1-128">The SignalR resource object.</span></span>

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

### <span data-ttu-id="20ae1-129">-Name</span><span class="sxs-lookup"><span data-stu-id="20ae1-129">-Name</span></span>
<span data-ttu-id="20ae1-130">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="20ae1-130">The SignalR service name.</span></span>

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

### <span data-ttu-id="20ae1-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="20ae1-131">-PrivateEndpointName</span></span>
<span data-ttu-id="20ae1-132">Nomi degli endpoint privati da aggiornare</span><span class="sxs-lookup"><span data-stu-id="20ae1-132">Name(s) of private endpoint(s) to be updated</span></span>

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

### <span data-ttu-id="20ae1-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="20ae1-133">-PublicNetwork</span></span>
<span data-ttu-id="20ae1-134">Aggiornare gli ACL di rete pubblica</span><span class="sxs-lookup"><span data-stu-id="20ae1-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="20ae1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20ae1-135">-ResourceGroupName</span></span>
<span data-ttu-id="20ae1-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="20ae1-136">The resource group name.</span></span>
<span data-ttu-id="20ae1-137">Se non è specificato, verrà usato quello predefinito.</span><span class="sxs-lookup"><span data-stu-id="20ae1-137">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="20ae1-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20ae1-138">-ResourceId</span></span>
<span data-ttu-id="20ae1-139">ID risorsa servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="20ae1-139">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="20ae1-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20ae1-140">-Confirm</span></span>
<span data-ttu-id="20ae1-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ae1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20ae1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20ae1-142">-WhatIf</span></span>
<span data-ttu-id="20ae1-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20ae1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20ae1-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20ae1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20ae1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ae1-145">CommonParameters</span></span>
<span data-ttu-id="20ae1-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20ae1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ae1-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="20ae1-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ae1-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="20ae1-148">INPUTS</span></span>

### <span data-ttu-id="20ae1-149">System.String</span><span class="sxs-lookup"><span data-stu-id="20ae1-149">System.String</span></span>

## <span data-ttu-id="20ae1-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20ae1-150">OUTPUTS</span></span>

### <span data-ttu-id="20ae1-151">Microsoft.Azure.Commands.Signalr.Models.PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="20ae1-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="20ae1-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="20ae1-152">NOTES</span></span>

## <span data-ttu-id="20ae1-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20ae1-153">RELATED LINKS</span></span>
