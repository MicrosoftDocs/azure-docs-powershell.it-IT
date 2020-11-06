---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: f7bbe0c37d03a6db372c6c70da021160060a542a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520079"
---
# <span data-ttu-id="1f3f3-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="1f3f3-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="1f3f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="1f3f3-103">Crea una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="1f3f3-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f3f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f3f3-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [[-PrimaryKey] <String>] [[-SecondaryKey] <String>] [-Rights] <PSAccessRights>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f3f3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f3f3-105">DESCRIPTION</span></span>
<span data-ttu-id="1f3f3-106">Crea una chiave per il IotHub fornito.</span><span class="sxs-lookup"><span data-stu-id="1f3f3-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="1f3f3-107">I nomi di nome non sono univoci e devono essere gestiti con attenzione.</span><span class="sxs-lookup"><span data-stu-id="1f3f3-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="1f3f3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f3f3-108">EXAMPLES</span></span>

### <span data-ttu-id="1f3f3-109">Esempio 1 aggiungere una chiave a un IotHub</span><span class="sxs-lookup"><span data-stu-id="1f3f3-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="1f3f3-110">Crea una chiave denominata "myKey" per la iothub "myiothub" con le autorizzazioni di RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="1f3f3-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="1f3f3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f3f3-111">PARAMETERS</span></span>

### <span data-ttu-id="1f3f3-112">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="1f3f3-112">-KeyName</span></span>
<span data-ttu-id="1f3f3-113">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="1f3f3-113">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3f3-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f3f3-114">-Name</span></span>
<span data-ttu-id="1f3f3-115">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="1f3f3-115">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f3f3-116">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="1f3f3-116">-PrimaryKey</span></span>
<span data-ttu-id="1f3f3-117">Chiave primaria</span><span class="sxs-lookup"><span data-stu-id="1f3f3-117">The primary key</span></span>

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

### <span data-ttu-id="1f3f3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f3f3-118">-ResourceGroupName</span></span>
<span data-ttu-id="1f3f3-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1f3f3-119">Resource Group Name</span></span>

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

### <span data-ttu-id="1f3f3-120">-Diritti</span><span class="sxs-lookup"><span data-stu-id="1f3f3-120">-Rights</span></span>
<span data-ttu-id="1f3f3-121">Le autorizzazioni per questo IOTHub</span><span class="sxs-lookup"><span data-stu-id="1f3f3-121">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases: 
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3f3-122">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="1f3f3-122">-SecondaryKey</span></span>
<span data-ttu-id="1f3f3-123">Tasto secondario</span><span class="sxs-lookup"><span data-stu-id="1f3f3-123">The Secondary Key</span></span>

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

### <span data-ttu-id="1f3f3-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f3f3-124">-Confirm</span></span>
<span data-ttu-id="1f3f3-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f3f3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f3f3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f3f3-126">-WhatIf</span></span>
<span data-ttu-id="1f3f3-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f3f3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f3f3-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f3f3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f3f3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f3f3-129">-DefaultProfile</span></span>
<span data-ttu-id="1f3f3-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f3f3-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f3f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f3f3-131">CommonParameters</span></span>
<span data-ttu-id="1f3f3-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f3f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f3f3-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f3f3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f3f3-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f3f3-134">INPUTS</span></span>

### <span data-ttu-id="1f3f3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1f3f3-135">System.String</span></span>
<span data-ttu-id="1f3f3-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSAccessRights</span><span class="sxs-lookup"><span data-stu-id="1f3f3-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights</span></span>

## <span data-ttu-id="1f3f3-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f3f3-137">OUTPUTS</span></span>

### <span data-ttu-id="1f3f3-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1f3f3-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="1f3f3-139">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="1f3f3-139">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="1f3f3-140">Note</span><span class="sxs-lookup"><span data-stu-id="1f3f3-140">NOTES</span></span>

## <span data-ttu-id="1f3f3-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f3f3-141">RELATED LINKS</span></span>

