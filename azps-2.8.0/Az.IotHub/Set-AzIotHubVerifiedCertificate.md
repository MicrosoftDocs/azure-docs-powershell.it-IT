---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 868ca6f3f9f65fea5fd04dba1fc19d4db11bd65c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674188"
---
# <span data-ttu-id="b5e11-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="b5e11-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="b5e11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5e11-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e11-103">Verifica un certificato Hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="b5e11-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="b5e11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5e11-104">SYNTAX</span></span>

### <span data-ttu-id="b5e11-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5e11-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5e11-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b5e11-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5e11-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b5e11-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5e11-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5e11-108">DESCRIPTION</span></span>
<span data-ttu-id="b5e11-109">Verifica un certificato caricando un certificato di verifica contenente il codice di verifica ottenuto dal cmdlet Get-AzIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="b5e11-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="b5e11-110">Questo è l'ultimo passaggio del processo di prova del possesso.</span><span class="sxs-lookup"><span data-stu-id="b5e11-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="b5e11-111">Per una spiegazione dettagliata dei certificati della CA in Azure molto Hub, vedere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="b5e11-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="b5e11-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5e11-112">EXAMPLES</span></span>

### <span data-ttu-id="b5e11-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b5e11-113">Example 1</span></span>
```
PS C:\> Set-AzIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="b5e11-114">Verifica la proprietà della chiave privata del certificato.</span><span class="sxs-lookup"><span data-stu-id="b5e11-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="b5e11-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5e11-115">PARAMETERS</span></span>

### <span data-ttu-id="b5e11-116">-Certificate</span><span class="sxs-lookup"><span data-stu-id="b5e11-116">-CertificateName</span></span>
<span data-ttu-id="b5e11-117">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="b5e11-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="b5e11-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e11-118">-DefaultProfile</span></span>
<span data-ttu-id="b5e11-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5e11-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5e11-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="b5e11-120">-Etag</span></span>
<span data-ttu-id="b5e11-121">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="b5e11-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="b5e11-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5e11-122">-InputObject</span></span>
<span data-ttu-id="b5e11-123">Oggetto certificato</span><span class="sxs-lookup"><span data-stu-id="b5e11-123">Certificate Object</span></span>

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

### <span data-ttu-id="b5e11-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5e11-124">-Name</span></span>
<span data-ttu-id="b5e11-125">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="b5e11-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b5e11-126">-Path</span><span class="sxs-lookup"><span data-stu-id="b5e11-126">-Path</span></span>
<span data-ttu-id="b5e11-127">rappresentazione di base-64 del file certificato. cer di X509 o del percorso di file con estensione PEM.</span><span class="sxs-lookup"><span data-stu-id="b5e11-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="b5e11-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5e11-128">-ResourceGroupName</span></span>
<span data-ttu-id="b5e11-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b5e11-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b5e11-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5e11-130">-ResourceId</span></span>
<span data-ttu-id="b5e11-131">ID risorsa certificato</span><span class="sxs-lookup"><span data-stu-id="b5e11-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="b5e11-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b5e11-132">-Confirm</span></span>
<span data-ttu-id="b5e11-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5e11-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5e11-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5e11-134">-WhatIf</span></span>
<span data-ttu-id="b5e11-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5e11-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5e11-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5e11-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5e11-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e11-137">CommonParameters</span></span>
<span data-ttu-id="b5e11-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5e11-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e11-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5e11-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e11-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5e11-140">INPUTS</span></span>

### <span data-ttu-id="b5e11-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="b5e11-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="b5e11-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b5e11-142">System.String</span></span>

## <span data-ttu-id="b5e11-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5e11-143">OUTPUTS</span></span>

### <span data-ttu-id="b5e11-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="b5e11-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="b5e11-145">Note</span><span class="sxs-lookup"><span data-stu-id="b5e11-145">NOTES</span></span>

## <span data-ttu-id="b5e11-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5e11-146">RELATED LINKS</span></span>