---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: bf66b65eb54c8ed0a7f52bc3871fd80567513f59
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022268"
---
# <span data-ttu-id="9a087-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="9a087-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="9a087-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a087-102">SYNOPSIS</span></span>
<span data-ttu-id="9a087-103">Aggiungere un nuovo tipo di nodo al cluster esistente.</span><span class="sxs-lookup"><span data-stu-id="9a087-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="9a087-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a087-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a087-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a087-105">DESCRIPTION</span></span>
<span data-ttu-id="9a087-106">Aggiungere un nuovo tipo di nodo a un cluster esistente.</span><span class="sxs-lookup"><span data-stu-id="9a087-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="9a087-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a087-107">EXAMPLES</span></span>

### <span data-ttu-id="9a087-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9a087-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="9a087-109">Questo comando aggiunge un nuovo NodeType "N2" con una capacità di 5 e il nome dell'amministratore della VM è "amministratore".</span><span class="sxs-lookup"><span data-stu-id="9a087-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="9a087-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a087-110">PARAMETERS</span></span>

### <span data-ttu-id="9a087-111">-Capacità</span><span class="sxs-lookup"><span data-stu-id="9a087-111">-Capacity</span></span>
<span data-ttu-id="9a087-112">Capacità</span><span class="sxs-lookup"><span data-stu-id="9a087-112">Capacity</span></span>

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

### <span data-ttu-id="9a087-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a087-113">-DefaultProfile</span></span>
<span data-ttu-id="9a087-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a087-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a087-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="9a087-115">-DurabilityLevel</span></span>
<span data-ttu-id="9a087-116">Specifica il livello di durabilità di NodeType.</span><span class="sxs-lookup"><span data-stu-id="9a087-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="9a087-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a087-117">-Name</span></span>
<span data-ttu-id="9a087-118">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="9a087-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="9a087-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="9a087-119">-NodeType</span></span>
<span data-ttu-id="9a087-120">Nome del tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="9a087-120">The node type name</span></span>

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

### <span data-ttu-id="9a087-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a087-121">-ResourceGroupName</span></span>
<span data-ttu-id="9a087-122">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9a087-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9a087-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="9a087-123">-Tier</span></span>
<span data-ttu-id="9a087-124">Livello SKU VM</span><span class="sxs-lookup"><span data-stu-id="9a087-124">Vm Sku Tier</span></span>

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

### <span data-ttu-id="9a087-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="9a087-125">-VmPassword</span></span>
<span data-ttu-id="9a087-126">La password per l'accesso alla VM</span><span class="sxs-lookup"><span data-stu-id="9a087-126">The password for login to the Vm</span></span>

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

### <span data-ttu-id="9a087-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="9a087-127">-VmSku</span></span>
<span data-ttu-id="9a087-128">Nome Usk</span><span class="sxs-lookup"><span data-stu-id="9a087-128">The sku name</span></span>

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

### <span data-ttu-id="9a087-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="9a087-129">-VmUserName</span></span>
<span data-ttu-id="9a087-130">Nome utente per la registrazione in VM</span><span class="sxs-lookup"><span data-stu-id="9a087-130">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="9a087-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9a087-131">-Confirm</span></span>
<span data-ttu-id="9a087-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a087-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a087-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a087-133">-WhatIf</span></span>
<span data-ttu-id="9a087-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a087-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a087-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a087-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a087-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a087-136">CommonParameters</span></span>
<span data-ttu-id="9a087-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a087-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a087-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a087-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a087-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a087-139">INPUTS</span></span>

### <span data-ttu-id="9a087-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9a087-140">System.String</span></span>

### <span data-ttu-id="9a087-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9a087-141">System.Int32</span></span>

### <span data-ttu-id="9a087-142">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="9a087-142">System.Security.SecureString</span></span>

### <span data-ttu-id="9a087-143">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="9a087-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="9a087-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a087-144">OUTPUTS</span></span>

### <span data-ttu-id="9a087-145">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="9a087-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="9a087-146">Note</span><span class="sxs-lookup"><span data-stu-id="9a087-146">NOTES</span></span>

## <span data-ttu-id="9a087-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a087-147">RELATED LINKS</span></span>
