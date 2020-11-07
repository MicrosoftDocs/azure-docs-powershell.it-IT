---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
ms.openlocfilehash: 45afd8c7f690be7785a14d336fabe7ac52a6f44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520986"
---
# <span data-ttu-id="534fc-101">Set-AzureRmIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="534fc-101">Set-AzureRmIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="534fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="534fc-102">SYNOPSIS</span></span>
<span data-ttu-id="534fc-103">Verifica un certificato Hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="534fc-103">Verifies an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="534fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="534fc-104">SYNTAX</span></span>

### <span data-ttu-id="534fc-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="534fc-105">ResourceSet (Default)</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="534fc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="534fc-106">InputObjectSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="534fc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="534fc-107">ResourceIdSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="534fc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="534fc-108">DESCRIPTION</span></span>
<span data-ttu-id="534fc-109">Verifica un certificato caricando un certificato di verifica contenente il codice di verifica ottenuto dal cmdlet Get-AzureRmIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="534fc-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzureRmIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="534fc-110">Questo è l'ultimo passaggio del processo di prova del possesso.</span><span class="sxs-lookup"><span data-stu-id="534fc-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="534fc-111">Per una spiegazione dettagliata dei certificati della CA in Azure molto Hub, vedere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="534fc-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="534fc-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="534fc-112">EXAMPLES</span></span>

### <span data-ttu-id="534fc-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="534fc-113">Example 1</span></span>
```
PS C:\> Set-AzureRmIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="534fc-114">Verifica la proprietà della chiave privata del certificato.</span><span class="sxs-lookup"><span data-stu-id="534fc-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="534fc-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="534fc-115">PARAMETERS</span></span>

### <span data-ttu-id="534fc-116">-Certificate</span><span class="sxs-lookup"><span data-stu-id="534fc-116">-CertificateName</span></span>
<span data-ttu-id="534fc-117">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="534fc-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="534fc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="534fc-118">-DefaultProfile</span></span>
<span data-ttu-id="534fc-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="534fc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="534fc-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="534fc-120">-Etag</span></span>
<span data-ttu-id="534fc-121">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="534fc-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="534fc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="534fc-122">-InputObject</span></span>
<span data-ttu-id="534fc-123">Oggetto certificato</span><span class="sxs-lookup"><span data-stu-id="534fc-123">Certificate Object</span></span>

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

### <span data-ttu-id="534fc-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="534fc-124">-Name</span></span>
<span data-ttu-id="534fc-125">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="534fc-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="534fc-126">-Path</span><span class="sxs-lookup"><span data-stu-id="534fc-126">-Path</span></span>
<span data-ttu-id="534fc-127">rappresentazione di base-64 del file certificato. cer di X509 o del percorso di file con estensione PEM.</span><span class="sxs-lookup"><span data-stu-id="534fc-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="534fc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="534fc-128">-ResourceGroupName</span></span>
<span data-ttu-id="534fc-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="534fc-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="534fc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="534fc-130">-ResourceId</span></span>
<span data-ttu-id="534fc-131">ID risorsa certificato</span><span class="sxs-lookup"><span data-stu-id="534fc-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="534fc-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="534fc-132">-Confirm</span></span>
<span data-ttu-id="534fc-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="534fc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="534fc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="534fc-134">-WhatIf</span></span>
<span data-ttu-id="534fc-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="534fc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="534fc-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="534fc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="534fc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="534fc-137">CommonParameters</span></span>
<span data-ttu-id="534fc-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="534fc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="534fc-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="534fc-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="534fc-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="534fc-140">INPUTS</span></span>

### <span data-ttu-id="534fc-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="534fc-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="534fc-142">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="534fc-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="534fc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="534fc-143">System.String</span></span>

## <span data-ttu-id="534fc-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="534fc-144">OUTPUTS</span></span>

### <span data-ttu-id="534fc-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="534fc-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="534fc-146">Note</span><span class="sxs-lookup"><span data-stu-id="534fc-146">NOTES</span></span>

## <span data-ttu-id="534fc-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="534fc-147">RELATED LINKS</span></span>