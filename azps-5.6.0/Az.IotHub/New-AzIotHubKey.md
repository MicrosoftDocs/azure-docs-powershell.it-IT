---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: 7dd27544e3304570cf3fbdae861b21eabd300c35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968974"
---
# <span data-ttu-id="5bfe5-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="5bfe5-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="5bfe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bfe5-102">SYNOPSIS</span></span>
<span data-ttu-id="5bfe5-103">Generare una chiave di Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="5bfe5-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="5bfe5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5bfe5-104">SYNTAX</span></span>

### <span data-ttu-id="5bfe5-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5bfe5-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bfe5-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5bfe5-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bfe5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5bfe5-107">DESCRIPTION</span></span>
<span data-ttu-id="5bfe5-108">Generare una chiave di Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="5bfe5-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="5bfe5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5bfe5-109">EXAMPLES</span></span>

### <span data-ttu-id="5bfe5-110">Esempio 1 Rigenerare la chiave primaria</span><span class="sxs-lookup"><span data-stu-id="5bfe5-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="5bfe5-111">Chiave primaria rigenerata per il criterio di autorizzazione "testKey" di un hub azure iot.</span><span class="sxs-lookup"><span data-stu-id="5bfe5-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="5bfe5-112">Esempio 2 Scambio di tasti</span><span class="sxs-lookup"><span data-stu-id="5bfe5-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="5bfe5-113">Scambio di chiavi con il criterio di autorizzazione "testKey" di un hub azure iot.</span><span class="sxs-lookup"><span data-stu-id="5bfe5-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="5bfe5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bfe5-114">PARAMETERS</span></span>

### <span data-ttu-id="5bfe5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bfe5-115">-DefaultProfile</span></span>
<span data-ttu-id="5bfe5-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5bfe5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bfe5-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="5bfe5-117">-HubId</span></span>
<span data-ttu-id="5bfe5-118">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="5bfe5-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5bfe5-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="5bfe5-119">-KeyName</span></span>
<span data-ttu-id="5bfe5-120">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="5bfe5-120">Name of the Key</span></span>

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

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bfe5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5bfe5-121">-Name</span></span>
<span data-ttu-id="5bfe5-122">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="5bfe5-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="5bfe5-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="5bfe5-123">-RenewKey</span></span>
<span data-ttu-id="5bfe5-124">Rigenerare chiave.</span><span class="sxs-lookup"><span data-stu-id="5bfe5-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="5bfe5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bfe5-125">-ResourceGroupName</span></span>
<span data-ttu-id="5bfe5-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5bfe5-126">Resource Group Name</span></span>

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

### <span data-ttu-id="5bfe5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bfe5-127">-Confirm</span></span>
<span data-ttu-id="5bfe5-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bfe5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bfe5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bfe5-129">-WhatIf</span></span>
<span data-ttu-id="5bfe5-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5bfe5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bfe5-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5bfe5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bfe5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bfe5-132">CommonParameters</span></span>
<span data-ttu-id="5bfe5-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bfe5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bfe5-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bfe5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bfe5-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="5bfe5-135">INPUTS</span></span>

### <span data-ttu-id="5bfe5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5bfe5-136">System.String</span></span>

## <span data-ttu-id="5bfe5-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5bfe5-137">OUTPUTS</span></span>

### <span data-ttu-id="5bfe5-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5bfe5-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="5bfe5-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="5bfe5-139">NOTES</span></span>

## <span data-ttu-id="5bfe5-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5bfe5-140">RELATED LINKS</span></span>
