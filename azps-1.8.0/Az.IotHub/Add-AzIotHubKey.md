---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: f73cfd1cadff449289bfa82ab1de04d110fb0f1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835927"
---
# <span data-ttu-id="88e98-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="88e98-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="88e98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88e98-102">SYNOPSIS</span></span>
<span data-ttu-id="88e98-103">Crea una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="88e98-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="88e98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88e98-104">SYNTAX</span></span>

```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88e98-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88e98-105">DESCRIPTION</span></span>
<span data-ttu-id="88e98-106">Crea una chiave per il IotHub fornito.</span><span class="sxs-lookup"><span data-stu-id="88e98-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="88e98-107">I nomi di nome non sono univoci e devono essere gestiti con attenzione.</span><span class="sxs-lookup"><span data-stu-id="88e98-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="88e98-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88e98-108">EXAMPLES</span></span>

### <span data-ttu-id="88e98-109">Esempio 1 aggiungere una chiave a un IotHub</span><span class="sxs-lookup"><span data-stu-id="88e98-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="88e98-110">Crea una chiave denominata "myKey" per la iothub "myiothub" con le autorizzazioni di RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="88e98-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="88e98-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88e98-111">PARAMETERS</span></span>

### <span data-ttu-id="88e98-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e98-112">-DefaultProfile</span></span>
<span data-ttu-id="88e98-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="88e98-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88e98-114">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="88e98-114">-KeyName</span></span>
<span data-ttu-id="88e98-115">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="88e98-115">Name of the Key</span></span>

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

### <span data-ttu-id="88e98-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="88e98-116">-Name</span></span>
<span data-ttu-id="88e98-117">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="88e98-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="88e98-118">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="88e98-118">-PrimaryKey</span></span>
<span data-ttu-id="88e98-119">Chiave primaria</span><span class="sxs-lookup"><span data-stu-id="88e98-119">The primary key</span></span>

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

### <span data-ttu-id="88e98-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88e98-120">-ResourceGroupName</span></span>
<span data-ttu-id="88e98-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="88e98-121">Resource Group Name</span></span>

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

### <span data-ttu-id="88e98-122">-Diritti</span><span class="sxs-lookup"><span data-stu-id="88e98-122">-Rights</span></span>
<span data-ttu-id="88e98-123">Le autorizzazioni per questo IOTHub</span><span class="sxs-lookup"><span data-stu-id="88e98-123">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="88e98-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="88e98-124">-SecondaryKey</span></span>
<span data-ttu-id="88e98-125">Tasto secondario</span><span class="sxs-lookup"><span data-stu-id="88e98-125">The Secondary Key</span></span>

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

### <span data-ttu-id="88e98-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="88e98-126">-Confirm</span></span>
<span data-ttu-id="88e98-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88e98-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88e98-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88e98-128">-WhatIf</span></span>
<span data-ttu-id="88e98-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88e98-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88e98-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88e98-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88e98-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e98-131">CommonParameters</span></span>
<span data-ttu-id="88e98-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88e98-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e98-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e98-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e98-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88e98-134">INPUTS</span></span>

### <span data-ttu-id="88e98-135">System. String</span><span class="sxs-lookup"><span data-stu-id="88e98-135">System.String</span></span>

## <span data-ttu-id="88e98-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88e98-136">OUTPUTS</span></span>

### <span data-ttu-id="88e98-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="88e98-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="88e98-138">Note</span><span class="sxs-lookup"><span data-stu-id="88e98-138">NOTES</span></span>

## <span data-ttu-id="88e98-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88e98-139">RELATED LINKS</span></span>
