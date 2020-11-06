---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: c56b147c5ac62e376eff1159eb679c5a692eb1b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518112"
---
# <span data-ttu-id="0971d-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="0971d-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="0971d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0971d-102">SYNOPSIS</span></span>
<span data-ttu-id="0971d-103">Crea una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="0971d-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0971d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0971d-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0971d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0971d-105">DESCRIPTION</span></span>
<span data-ttu-id="0971d-106">Crea una chiave per il IotHub fornito.</span><span class="sxs-lookup"><span data-stu-id="0971d-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="0971d-107">I nomi di nome non sono univoci e devono essere gestiti con attenzione.</span><span class="sxs-lookup"><span data-stu-id="0971d-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="0971d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0971d-108">EXAMPLES</span></span>

### <span data-ttu-id="0971d-109">Esempio 1 aggiungere una chiave a un IotHub</span><span class="sxs-lookup"><span data-stu-id="0971d-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="0971d-110">Crea una chiave denominata "myKey" per la iothub "myiothub" con le autorizzazioni di RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="0971d-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="0971d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0971d-111">PARAMETERS</span></span>

### <span data-ttu-id="0971d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0971d-112">-DefaultProfile</span></span>
<span data-ttu-id="0971d-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0971d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0971d-114">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="0971d-114">-KeyName</span></span>
<span data-ttu-id="0971d-115">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="0971d-115">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0971d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0971d-116">-Name</span></span>
<span data-ttu-id="0971d-117">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="0971d-117">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0971d-118">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="0971d-118">-PrimaryKey</span></span>
<span data-ttu-id="0971d-119">Chiave primaria</span><span class="sxs-lookup"><span data-stu-id="0971d-119">The primary key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0971d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0971d-120">-ResourceGroupName</span></span>
<span data-ttu-id="0971d-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="0971d-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0971d-122">-Diritti</span><span class="sxs-lookup"><span data-stu-id="0971d-122">-Rights</span></span>
<span data-ttu-id="0971d-123">Le autorizzazioni per questo IOTHub</span><span class="sxs-lookup"><span data-stu-id="0971d-123">The permissions for this IOTHub</span></span>

```yaml
Type: PSAccessRights
Parameter Sets: (All)
Aliases: 
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0971d-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="0971d-124">-SecondaryKey</span></span>
<span data-ttu-id="0971d-125">Tasto secondario</span><span class="sxs-lookup"><span data-stu-id="0971d-125">The Secondary Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0971d-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0971d-126">-Confirm</span></span>
<span data-ttu-id="0971d-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0971d-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0971d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0971d-128">-WhatIf</span></span>
<span data-ttu-id="0971d-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0971d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0971d-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0971d-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0971d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0971d-131">CommonParameters</span></span>
<span data-ttu-id="0971d-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0971d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0971d-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0971d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0971d-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0971d-134">INPUTS</span></span>

### <span data-ttu-id="0971d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0971d-135">System.String</span></span>
<span data-ttu-id="0971d-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSAccessRights</span><span class="sxs-lookup"><span data-stu-id="0971d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights</span></span>

## <span data-ttu-id="0971d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0971d-137">OUTPUTS</span></span>

### <span data-ttu-id="0971d-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0971d-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="0971d-139">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="0971d-139">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="0971d-140">Note</span><span class="sxs-lookup"><span data-stu-id="0971d-140">NOTES</span></span>

## <span data-ttu-id="0971d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0971d-141">RELATED LINKS</span></span>

