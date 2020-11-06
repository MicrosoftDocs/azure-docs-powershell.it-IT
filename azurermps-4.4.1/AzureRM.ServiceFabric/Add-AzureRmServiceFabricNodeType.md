---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 305e406a3f2ef723eb0431b495106bb688ffe61c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519509"
---
# <span data-ttu-id="4b518-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="4b518-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="4b518-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b518-102">SYNOPSIS</span></span>
<span data-ttu-id="4b518-103">Aggiungere un nuovo tipo di nodo al cluster esistente.</span><span class="sxs-lookup"><span data-stu-id="4b518-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b518-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b518-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -Capacity <Int32> -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b518-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b518-105">DESCRIPTION</span></span>
<span data-ttu-id="4b518-106">Aggiungere un nuovo tipo di nodo a un cluster esistente.</span><span class="sxs-lookup"><span data-stu-id="4b518-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="4b518-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b518-107">EXAMPLES</span></span>

### <span data-ttu-id="4b518-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4b518-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="4b518-109">Questo comando aggiunge un nuovo NodeType "N2" con una capacità di 5 e il nome dell'amministratore della VM è "amministratore".</span><span class="sxs-lookup"><span data-stu-id="4b518-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="4b518-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b518-110">PARAMETERS</span></span>

### <span data-ttu-id="4b518-111">-Capacità</span><span class="sxs-lookup"><span data-stu-id="4b518-111">-Capacity</span></span>
<span data-ttu-id="4b518-112">Capacità</span><span class="sxs-lookup"><span data-stu-id="4b518-112">Capacity</span></span>

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

### <span data-ttu-id="4b518-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b518-113">-Name</span></span>
<span data-ttu-id="4b518-114">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="4b518-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4b518-115">-NodeType</span><span class="sxs-lookup"><span data-stu-id="4b518-115">-NodeType</span></span>
<span data-ttu-id="4b518-116">Nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="4b518-116">The node type name.</span></span>

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

### <span data-ttu-id="4b518-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b518-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b518-118">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b518-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4b518-119">-Tier</span><span class="sxs-lookup"><span data-stu-id="4b518-119">-Tier</span></span>
<span data-ttu-id="4b518-120">Livello SKU VM.</span><span class="sxs-lookup"><span data-stu-id="4b518-120">Vm Sku Tier.</span></span>

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

### <span data-ttu-id="4b518-121">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="4b518-121">-DurabilityLevel</span></span>
<span data-ttu-id="4b518-122">Specifica il livello di durabilità di NodeType.</span><span class="sxs-lookup"><span data-stu-id="4b518-122">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="4b518-123">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="4b518-123">-VmPassword</span></span>
<span data-ttu-id="4b518-124">La password di accesso alla VM.</span><span class="sxs-lookup"><span data-stu-id="4b518-124">The password of login to the Vm.</span></span>

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

### <span data-ttu-id="4b518-125">-VmSku</span><span class="sxs-lookup"><span data-stu-id="4b518-125">-VmSku</span></span>
<span data-ttu-id="4b518-126">Nome Usk.</span><span class="sxs-lookup"><span data-stu-id="4b518-126">The sku name.</span></span>

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

### <span data-ttu-id="4b518-127">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="4b518-127">-VmUserName</span></span>
<span data-ttu-id="4b518-128">Nome utente per l'accesso a VM.</span><span class="sxs-lookup"><span data-stu-id="4b518-128">The user name for login to Vm.</span></span>

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

### <span data-ttu-id="4b518-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4b518-129">-Confirm</span></span>
<span data-ttu-id="4b518-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b518-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b518-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b518-131">-WhatIf</span></span>
<span data-ttu-id="4b518-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b518-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b518-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b518-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b518-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b518-134">-DefaultProfile</span></span>
<span data-ttu-id="4b518-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b518-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b518-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b518-136">CommonParameters</span></span>
<span data-ttu-id="4b518-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b518-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b518-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b518-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b518-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b518-139">INPUTS</span></span>

### <span data-ttu-id="4b518-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4b518-140">System.String</span></span>
<span data-ttu-id="4b518-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4b518-141">System.Int32</span></span>

## <span data-ttu-id="4b518-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b518-142">OUTPUTS</span></span>

### <span data-ttu-id="4b518-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="4b518-143">System.Object</span></span>

## <span data-ttu-id="4b518-144">Note</span><span class="sxs-lookup"><span data-stu-id="4b518-144">NOTES</span></span>

## <span data-ttu-id="4b518-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b518-145">RELATED LINKS</span></span>

