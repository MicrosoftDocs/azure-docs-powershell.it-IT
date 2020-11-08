---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021964"
---
# <span data-ttu-id="ca859-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca859-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="ca859-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca859-102">SYNOPSIS</span></span>
<span data-ttu-id="ca859-103">Rimuove una connessione di endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="ca859-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="ca859-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca859-104">SYNTAX</span></span>

### <span data-ttu-id="ca859-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca859-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca859-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="ca859-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca859-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca859-107">DESCRIPTION</span></span>
<span data-ttu-id="ca859-108">Il cmdlet **Remove-AzPrivateEndpointConnection** rimuove una connessione endpoint privata.</span><span class="sxs-lookup"><span data-stu-id="ca859-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="ca859-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca859-109">EXAMPLES</span></span>

### <span data-ttu-id="ca859-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ca859-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="ca859-111">Questo esempio rimuove una connessione di endpoint privato denominata MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="ca859-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="ca859-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca859-112">PARAMETERS</span></span>

### <span data-ttu-id="ca859-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca859-113">-AsJob</span></span>
<span data-ttu-id="ca859-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ca859-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca859-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca859-115">-DefaultProfile</span></span>
<span data-ttu-id="ca859-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca859-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca859-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ca859-117">-Force</span></span>
<span data-ttu-id="ca859-118">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="ca859-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="ca859-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca859-119">-Name</span></span>
<span data-ttu-id="ca859-120">Nome della connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="ca859-120">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca859-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca859-121">-PassThru</span></span>
<span data-ttu-id="ca859-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ca859-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ca859-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ca859-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ca859-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="ca859-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="ca859-125">Tipo di risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="ca859-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca859-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca859-126">-ResourceGroupName</span></span>
<span data-ttu-id="ca859-127">Il nome del gruppo di risorse della connessione endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="ca859-127">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca859-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca859-128">-ResourceId</span></span>
<span data-ttu-id="ca859-129">ID di gestione risorse di Azure della connessione endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="ca859-129">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca859-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ca859-130">-ServiceName</span></span>
<span data-ttu-id="ca859-131">Nome del servizio a cui appartiene la connessione all'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="ca859-131">The name of service that the private endpoint connection belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca859-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca859-132">-Confirm</span></span>
<span data-ttu-id="ca859-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca859-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca859-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca859-134">-WhatIf</span></span>
<span data-ttu-id="ca859-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca859-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca859-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca859-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca859-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca859-137">CommonParameters</span></span>
<span data-ttu-id="ca859-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca859-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca859-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca859-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca859-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca859-140">INPUTS</span></span>

### <span data-ttu-id="ca859-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ca859-141">System.String</span></span>

## <span data-ttu-id="ca859-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca859-142">OUTPUTS</span></span>

### <span data-ttu-id="ca859-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca859-143">System.Boolean</span></span>

## <span data-ttu-id="ca859-144">Note</span><span class="sxs-lookup"><span data-stu-id="ca859-144">NOTES</span></span>

## <span data-ttu-id="ca859-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca859-145">RELATED LINKS</span></span>

[<span data-ttu-id="ca859-146">Approva-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca859-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="ca859-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca859-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="ca859-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca859-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="ca859-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca859-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
