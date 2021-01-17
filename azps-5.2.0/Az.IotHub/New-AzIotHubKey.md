---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: cc843ca942ae79fe76e1dd50e76c876e4d05b5ac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350371"
---
# <span data-ttu-id="d91ac-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="d91ac-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="d91ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d91ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d91ac-103">Genera una chiave Hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="d91ac-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="d91ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d91ac-104">SYNTAX</span></span>

### <span data-ttu-id="d91ac-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d91ac-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d91ac-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d91ac-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d91ac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d91ac-107">DESCRIPTION</span></span>
<span data-ttu-id="d91ac-108">Genera una chiave Hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="d91ac-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="d91ac-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d91ac-109">EXAMPLES</span></span>

### <span data-ttu-id="d91ac-110">Esempio 1 Rigenera chiave primaria</span><span class="sxs-lookup"><span data-stu-id="d91ac-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="d91ac-111">Chiave primaria rigenerata per i criteri di autorizzazione "testKey" di un hub di Azure.</span><span class="sxs-lookup"><span data-stu-id="d91ac-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="d91ac-112">Esempio 2 scambio di tasti</span><span class="sxs-lookup"><span data-stu-id="d91ac-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="d91ac-113">Scambio di chiavi per i criteri di autorizzazione "testKey" di un hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="d91ac-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="d91ac-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d91ac-114">PARAMETERS</span></span>

### <span data-ttu-id="d91ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d91ac-115">-DefaultProfile</span></span>
<span data-ttu-id="d91ac-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d91ac-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d91ac-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="d91ac-117">-HubId</span></span>
<span data-ttu-id="d91ac-118">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="d91ac-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d91ac-119">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="d91ac-119">-KeyName</span></span>
<span data-ttu-id="d91ac-120">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="d91ac-120">Name of the Key</span></span>

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

### <span data-ttu-id="d91ac-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d91ac-121">-Name</span></span>
<span data-ttu-id="d91ac-122">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="d91ac-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="d91ac-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="d91ac-123">-RenewKey</span></span>
<span data-ttu-id="d91ac-124">Tasto rigenera.</span><span class="sxs-lookup"><span data-stu-id="d91ac-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="d91ac-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d91ac-125">-ResourceGroupName</span></span>
<span data-ttu-id="d91ac-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d91ac-126">Resource Group Name</span></span>

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

### <span data-ttu-id="d91ac-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d91ac-127">-Confirm</span></span>
<span data-ttu-id="d91ac-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d91ac-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d91ac-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d91ac-129">-WhatIf</span></span>
<span data-ttu-id="d91ac-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d91ac-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d91ac-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d91ac-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d91ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d91ac-132">CommonParameters</span></span>
<span data-ttu-id="d91ac-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d91ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d91ac-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d91ac-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d91ac-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d91ac-135">INPUTS</span></span>

### <span data-ttu-id="d91ac-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d91ac-136">System.String</span></span>

## <span data-ttu-id="d91ac-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d91ac-137">OUTPUTS</span></span>

### <span data-ttu-id="d91ac-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d91ac-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="d91ac-139">Note</span><span class="sxs-lookup"><span data-stu-id="d91ac-139">NOTES</span></span>

## <span data-ttu-id="d91ac-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d91ac-140">RELATED LINKS</span></span>
