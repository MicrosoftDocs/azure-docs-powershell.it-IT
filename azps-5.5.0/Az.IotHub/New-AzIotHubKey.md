---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: cc843ca942ae79fe76e1dd50e76c876e4d05b5ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200103"
---
# <span data-ttu-id="aaa59-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="aaa59-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="aaa59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaa59-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa59-103">Generare una chiave di Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="aaa59-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="aaa59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aaa59-104">SYNTAX</span></span>

### <span data-ttu-id="aaa59-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aaa59-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaa59-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aaa59-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaa59-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aaa59-107">DESCRIPTION</span></span>
<span data-ttu-id="aaa59-108">Generare una chiave di Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="aaa59-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="aaa59-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aaa59-109">EXAMPLES</span></span>

### <span data-ttu-id="aaa59-110">Esempio 1 Rigenerare la chiave primaria</span><span class="sxs-lookup"><span data-stu-id="aaa59-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="aaa59-111">Chiave primaria rigenerata per il criterio di autorizzazione "testKey" di un hub azure iot.</span><span class="sxs-lookup"><span data-stu-id="aaa59-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="aaa59-112">Esempio 2 Scambio di tasti</span><span class="sxs-lookup"><span data-stu-id="aaa59-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="aaa59-113">Scambio di chiavi con il criterio di autorizzazione "testKey" di un hub azure iot.</span><span class="sxs-lookup"><span data-stu-id="aaa59-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="aaa59-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaa59-114">PARAMETERS</span></span>

### <span data-ttu-id="aaa59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa59-115">-DefaultProfile</span></span>
<span data-ttu-id="aaa59-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="aaa59-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaa59-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="aaa59-117">-HubId</span></span>
<span data-ttu-id="aaa59-118">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="aaa59-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="aaa59-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="aaa59-119">-KeyName</span></span>
<span data-ttu-id="aaa59-120">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="aaa59-120">Name of the Key</span></span>

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

### <span data-ttu-id="aaa59-121">-Name</span><span class="sxs-lookup"><span data-stu-id="aaa59-121">-Name</span></span>
<span data-ttu-id="aaa59-122">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="aaa59-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="aaa59-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="aaa59-123">-RenewKey</span></span>
<span data-ttu-id="aaa59-124">Rigenerare chiave.</span><span class="sxs-lookup"><span data-stu-id="aaa59-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="aaa59-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaa59-125">-ResourceGroupName</span></span>
<span data-ttu-id="aaa59-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="aaa59-126">Resource Group Name</span></span>

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

### <span data-ttu-id="aaa59-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aaa59-127">-Confirm</span></span>
<span data-ttu-id="aaa59-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaa59-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaa59-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaa59-129">-WhatIf</span></span>
<span data-ttu-id="aaa59-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaa59-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaa59-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaa59-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaa59-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa59-132">CommonParameters</span></span>
<span data-ttu-id="aaa59-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaa59-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa59-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaa59-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa59-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="aaa59-135">INPUTS</span></span>

### <span data-ttu-id="aaa59-136">System.String</span><span class="sxs-lookup"><span data-stu-id="aaa59-136">System.String</span></span>

## <span data-ttu-id="aaa59-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aaa59-137">OUTPUTS</span></span>

### <span data-ttu-id="aaa59-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="aaa59-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="aaa59-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="aaa59-139">NOTES</span></span>

## <span data-ttu-id="aaa59-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aaa59-140">RELATED LINKS</span></span>
