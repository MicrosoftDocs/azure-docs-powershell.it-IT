---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: 379aaa360776291515f1848cd48b24e88be23ef6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515240"
---
# <span data-ttu-id="b43d3-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="b43d3-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="b43d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b43d3-102">SYNOPSIS</span></span>
<span data-ttu-id="b43d3-103">Crea una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="b43d3-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b43d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b43d3-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b43d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b43d3-105">DESCRIPTION</span></span>
<span data-ttu-id="b43d3-106">Crea una chiave per il IotHub fornito.</span><span class="sxs-lookup"><span data-stu-id="b43d3-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="b43d3-107">I nomi di nome non sono univoci e devono essere gestiti con attenzione.</span><span class="sxs-lookup"><span data-stu-id="b43d3-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="b43d3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b43d3-108">EXAMPLES</span></span>

### <span data-ttu-id="b43d3-109">Esempio 1 aggiungere una chiave a un IotHub</span><span class="sxs-lookup"><span data-stu-id="b43d3-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="b43d3-110">Crea una chiave denominata "myKey" per la iothub "myiothub" con le autorizzazioni di RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="b43d3-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="b43d3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b43d3-111">PARAMETERS</span></span>

### <span data-ttu-id="b43d3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43d3-112">-DefaultProfile</span></span>
<span data-ttu-id="b43d3-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b43d3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b43d3-114">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="b43d3-114">-KeyName</span></span>
<span data-ttu-id="b43d3-115">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="b43d3-115">Name of the Key</span></span>

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

### <span data-ttu-id="b43d3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b43d3-116">-Name</span></span>
<span data-ttu-id="b43d3-117">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="b43d3-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="b43d3-118">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b43d3-118">-PrimaryKey</span></span>
<span data-ttu-id="b43d3-119">Chiave primaria</span><span class="sxs-lookup"><span data-stu-id="b43d3-119">The primary key</span></span>

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

### <span data-ttu-id="b43d3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b43d3-120">-ResourceGroupName</span></span>
<span data-ttu-id="b43d3-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b43d3-121">Resource Group Name</span></span>

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

### <span data-ttu-id="b43d3-122">-Diritti</span><span class="sxs-lookup"><span data-stu-id="b43d3-122">-Rights</span></span>
<span data-ttu-id="b43d3-123">Le autorizzazioni per questo IOTHub</span><span class="sxs-lookup"><span data-stu-id="b43d3-123">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="b43d3-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="b43d3-124">-SecondaryKey</span></span>
<span data-ttu-id="b43d3-125">Tasto secondario</span><span class="sxs-lookup"><span data-stu-id="b43d3-125">The Secondary Key</span></span>

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

### <span data-ttu-id="b43d3-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b43d3-126">-Confirm</span></span>
<span data-ttu-id="b43d3-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b43d3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b43d3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b43d3-128">-WhatIf</span></span>
<span data-ttu-id="b43d3-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b43d3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b43d3-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b43d3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b43d3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43d3-131">CommonParameters</span></span>
<span data-ttu-id="b43d3-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b43d3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43d3-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b43d3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43d3-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b43d3-134">INPUTS</span></span>

### <span data-ttu-id="b43d3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b43d3-135">System.String</span></span>

## <span data-ttu-id="b43d3-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b43d3-136">OUTPUTS</span></span>

### <span data-ttu-id="b43d3-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b43d3-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b43d3-138">Note</span><span class="sxs-lookup"><span data-stu-id="b43d3-138">NOTES</span></span>

## <span data-ttu-id="b43d3-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b43d3-139">RELATED LINKS</span></span>
