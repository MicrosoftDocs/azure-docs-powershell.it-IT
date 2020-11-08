---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 422eb25456beb57ed6ab029fa5d70a47061ca491
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189921"
---
# <span data-ttu-id="d4637-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="d4637-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="d4637-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4637-102">SYNOPSIS</span></span>
<span data-ttu-id="d4637-103">Crea una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="d4637-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="d4637-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4637-104">SYNTAX</span></span>

### <span data-ttu-id="d4637-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4637-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4637-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d4637-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4637-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4637-107">DESCRIPTION</span></span>
<span data-ttu-id="d4637-108">Crea una chiave per il IotHub fornito.</span><span class="sxs-lookup"><span data-stu-id="d4637-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="d4637-109">I nomi di nome non sono univoci e devono essere gestiti con attenzione.</span><span class="sxs-lookup"><span data-stu-id="d4637-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="d4637-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4637-110">EXAMPLES</span></span>

### <span data-ttu-id="d4637-111">Esempio 1 aggiungere una chiave a un IotHub</span><span class="sxs-lookup"><span data-stu-id="d4637-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="d4637-112">Crea una chiave denominata "myKey" per la iothub "myiothub" con le autorizzazioni di RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="d4637-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="d4637-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4637-113">PARAMETERS</span></span>

### <span data-ttu-id="d4637-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4637-114">-DefaultProfile</span></span>
<span data-ttu-id="d4637-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d4637-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4637-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="d4637-116">-HubId</span></span>
<span data-ttu-id="d4637-117">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="d4637-117">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4637-118">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="d4637-118">-KeyName</span></span>
<span data-ttu-id="d4637-119">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="d4637-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4637-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4637-120">-Name</span></span>
<span data-ttu-id="d4637-121">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="d4637-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4637-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="d4637-122">-PrimaryKey</span></span>
<span data-ttu-id="d4637-123">Chiave primaria</span><span class="sxs-lookup"><span data-stu-id="d4637-123">The primary key</span></span>

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

### <span data-ttu-id="d4637-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4637-124">-ResourceGroupName</span></span>
<span data-ttu-id="d4637-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d4637-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4637-126">-Diritti</span><span class="sxs-lookup"><span data-stu-id="d4637-126">-Rights</span></span>
<span data-ttu-id="d4637-127">Le autorizzazioni per questo IOTHub</span><span class="sxs-lookup"><span data-stu-id="d4637-127">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4637-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="d4637-128">-SecondaryKey</span></span>
<span data-ttu-id="d4637-129">Tasto secondario</span><span class="sxs-lookup"><span data-stu-id="d4637-129">The Secondary Key</span></span>

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

### <span data-ttu-id="d4637-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d4637-130">-Confirm</span></span>
<span data-ttu-id="d4637-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4637-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4637-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4637-132">-WhatIf</span></span>
<span data-ttu-id="d4637-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4637-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4637-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4637-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4637-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4637-135">CommonParameters</span></span>
<span data-ttu-id="d4637-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4637-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4637-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4637-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4637-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4637-138">INPUTS</span></span>

### <span data-ttu-id="d4637-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d4637-139">System.String</span></span>

## <span data-ttu-id="d4637-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4637-140">OUTPUTS</span></span>

### <span data-ttu-id="d4637-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d4637-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="d4637-142">Note</span><span class="sxs-lookup"><span data-stu-id="d4637-142">NOTES</span></span>

## <span data-ttu-id="d4637-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4637-143">RELATED LINKS</span></span>