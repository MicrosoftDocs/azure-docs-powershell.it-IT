---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: 3e30b7aa3d1e43844fc1fe53e860ee8b8c66f385
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193294"
---
# <span data-ttu-id="28cef-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="28cef-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="28cef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28cef-102">SYNOPSIS</span></span>
<span data-ttu-id="28cef-103">Elimina un certificato Hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="28cef-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="28cef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28cef-104">SYNTAX</span></span>

### <span data-ttu-id="28cef-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="28cef-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28cef-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="28cef-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28cef-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="28cef-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28cef-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28cef-108">DESCRIPTION</span></span>
<span data-ttu-id="28cef-109">Per una spiegazione dettagliata dei certificati della CA in Azure molto Hub, vedere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="28cef-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="28cef-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28cef-110">EXAMPLES</span></span>

### <span data-ttu-id="28cef-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28cef-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="28cef-112">Elimina il certificato</span><span class="sxs-lookup"><span data-stu-id="28cef-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="28cef-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28cef-113">PARAMETERS</span></span>

### <span data-ttu-id="28cef-114">-Certificate</span><span class="sxs-lookup"><span data-stu-id="28cef-114">-CertificateName</span></span>
<span data-ttu-id="28cef-115">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="28cef-115">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28cef-116">-DefaultProfile</span></span>
<span data-ttu-id="28cef-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28cef-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28cef-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="28cef-118">-Etag</span></span>
<span data-ttu-id="28cef-119">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="28cef-119">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cef-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28cef-120">-InputObject</span></span>
<span data-ttu-id="28cef-121">Oggetto certificato</span><span class="sxs-lookup"><span data-stu-id="28cef-121">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28cef-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="28cef-122">-Name</span></span>
<span data-ttu-id="28cef-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="28cef-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="28cef-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28cef-124">-PassThru</span></span>
<span data-ttu-id="28cef-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="28cef-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28cef-126">-ResourceGroupName</span></span>
<span data-ttu-id="28cef-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="28cef-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="28cef-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28cef-128">-ResourceId</span></span>
<span data-ttu-id="28cef-129">ID risorsa certificato</span><span class="sxs-lookup"><span data-stu-id="28cef-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="28cef-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="28cef-130">-Confirm</span></span>
<span data-ttu-id="28cef-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28cef-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28cef-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28cef-132">-WhatIf</span></span>
<span data-ttu-id="28cef-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28cef-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28cef-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28cef-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28cef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28cef-135">CommonParameters</span></span>
<span data-ttu-id="28cef-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28cef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28cef-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28cef-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28cef-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28cef-138">INPUTS</span></span>

### <span data-ttu-id="28cef-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="28cef-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="28cef-140">System. String</span><span class="sxs-lookup"><span data-stu-id="28cef-140">System.String</span></span>

## <span data-ttu-id="28cef-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28cef-141">OUTPUTS</span></span>

### <span data-ttu-id="28cef-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28cef-142">System.Boolean</span></span>

## <span data-ttu-id="28cef-143">Note</span><span class="sxs-lookup"><span data-stu-id="28cef-143">NOTES</span></span>

## <span data-ttu-id="28cef-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28cef-144">RELATED LINKS</span></span>
