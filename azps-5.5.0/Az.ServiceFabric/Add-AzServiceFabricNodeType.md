---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: de512f636b0a326029981e199b13926a9fc5824a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208082"
---
# <span data-ttu-id="616e8-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="616e8-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="616e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="616e8-102">SYNOPSIS</span></span>
<span data-ttu-id="616e8-103">Aggiungere un nuovo tipo di nodo al cluster esistente.</span><span class="sxs-lookup"><span data-stu-id="616e8-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="616e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="616e8-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="616e8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="616e8-105">DESCRIPTION</span></span>
<span data-ttu-id="616e8-106">Aggiungere un nuovo tipo di nodo a un cluster esistente.</span><span class="sxs-lookup"><span data-stu-id="616e8-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="616e8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="616e8-107">EXAMPLES</span></span>

### <span data-ttu-id="616e8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="616e8-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="616e8-109">Questo comando aggiunge un nuovo NodeType 'n2' con capacità di 5 e il nome amministratore della macchina virtuale è 'adminName'.</span><span class="sxs-lookup"><span data-stu-id="616e8-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="616e8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="616e8-110">PARAMETERS</span></span>

### <span data-ttu-id="616e8-111">-Capacità</span><span class="sxs-lookup"><span data-stu-id="616e8-111">-Capacity</span></span>
<span data-ttu-id="616e8-112">Capacità</span><span class="sxs-lookup"><span data-stu-id="616e8-112">Capacity</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="616e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="616e8-113">-DefaultProfile</span></span>
<span data-ttu-id="616e8-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="616e8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="616e8-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="616e8-115">-DurabilityLevel</span></span>
<span data-ttu-id="616e8-116">Specificare il livello di durabilità di NodeType.</span><span class="sxs-lookup"><span data-stu-id="616e8-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases:
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="616e8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="616e8-117">-Name</span></span>
<span data-ttu-id="616e8-118">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="616e8-118">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616e8-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="616e8-119">-NodeType</span></span>
<span data-ttu-id="616e8-120">Nome del tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="616e8-120">The node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="616e8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="616e8-121">-ResourceGroupName</span></span>
<span data-ttu-id="616e8-122">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="616e8-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616e8-123">-Livello</span><span class="sxs-lookup"><span data-stu-id="616e8-123">-Tier</span></span>
<span data-ttu-id="616e8-124">Vm Sku Tier</span><span class="sxs-lookup"><span data-stu-id="616e8-124">Vm Sku Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="616e8-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="616e8-125">-VmPassword</span></span>
<span data-ttu-id="616e8-126">La password per l'accesso alla macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="616e8-126">The password for login to the Vm</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="616e8-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="616e8-127">-VmSku</span></span>
<span data-ttu-id="616e8-128">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="616e8-128">The sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="616e8-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="616e8-129">-VmUserName</span></span>
<span data-ttu-id="616e8-130">Nome utente per la registrazione alla macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="616e8-130">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="616e8-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="616e8-131">-Confirm</span></span>
<span data-ttu-id="616e8-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="616e8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="616e8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="616e8-133">-WhatIf</span></span>
<span data-ttu-id="616e8-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="616e8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="616e8-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="616e8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="616e8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="616e8-136">CommonParameters</span></span>
<span data-ttu-id="616e8-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="616e8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="616e8-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="616e8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="616e8-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="616e8-139">INPUTS</span></span>

### <span data-ttu-id="616e8-140">System.String</span><span class="sxs-lookup"><span data-stu-id="616e8-140">System.String</span></span>

### <span data-ttu-id="616e8-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="616e8-141">System.Int32</span></span>

### <span data-ttu-id="616e8-142">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="616e8-142">System.Security.SecureString</span></span>

### <span data-ttu-id="616e8-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="616e8-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="616e8-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="616e8-144">OUTPUTS</span></span>

### <span data-ttu-id="616e8-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="616e8-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="616e8-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="616e8-146">NOTES</span></span>

## <span data-ttu-id="616e8-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="616e8-147">RELATED LINKS</span></span>
