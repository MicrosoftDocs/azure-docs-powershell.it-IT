---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 5e887dc2f608dd7e26c05e3b7ca73036efe2595a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004094"
---
# <span data-ttu-id="37f82-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="37f82-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="37f82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37f82-102">SYNOPSIS</span></span>
<span data-ttu-id="37f82-103">Verifica un certificato hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="37f82-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="37f82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37f82-104">SYNTAX</span></span>

### <span data-ttu-id="37f82-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="37f82-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37f82-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="37f82-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37f82-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="37f82-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37f82-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="37f82-108">DESCRIPTION</span></span>
<span data-ttu-id="37f82-109">Verifica un certificato caricando un certificato di verifica contenente il codice di verifica ottenuto dal cmdlet Get-AzIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="37f82-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="37f82-110">Questo è l'ultimo passaggio della prova del processo di approvazione.</span><span class="sxs-lookup"><span data-stu-id="37f82-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="37f82-111">Per una spiegazione dettagliata dei certificati CA nell'Hub IoT di Azure, vedi https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="37f82-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="37f82-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37f82-112">EXAMPLES</span></span>

### <span data-ttu-id="37f82-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="37f82-113">Example 1</span></span>
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

<span data-ttu-id="37f82-114">Verifica la proprietà della chiave privata MyCertificate.</span><span class="sxs-lookup"><span data-stu-id="37f82-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="37f82-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37f82-115">PARAMETERS</span></span>

### <span data-ttu-id="37f82-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="37f82-116">-CertificateName</span></span>
<span data-ttu-id="37f82-117">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="37f82-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="37f82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f82-118">-DefaultProfile</span></span>
<span data-ttu-id="37f82-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37f82-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37f82-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="37f82-120">-Etag</span></span>
<span data-ttu-id="37f82-121">Etag del certificato</span><span class="sxs-lookup"><span data-stu-id="37f82-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="37f82-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37f82-122">-InputObject</span></span>
<span data-ttu-id="37f82-123">Oggetto Certificate</span><span class="sxs-lookup"><span data-stu-id="37f82-123">Certificate Object</span></span>

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

### <span data-ttu-id="37f82-124">-Name</span><span class="sxs-lookup"><span data-stu-id="37f82-124">-Name</span></span>
<span data-ttu-id="37f82-125">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="37f82-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="37f82-126">-Path</span><span class="sxs-lookup"><span data-stu-id="37f82-126">-Path</span></span>
<span data-ttu-id="37f82-127">Rappresentazione in base 64 del file CON ESTENSIONE CER o PEM del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="37f82-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="37f82-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37f82-128">-ResourceGroupName</span></span>
<span data-ttu-id="37f82-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="37f82-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="37f82-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37f82-130">-ResourceId</span></span>
<span data-ttu-id="37f82-131">ID risorsa certificato</span><span class="sxs-lookup"><span data-stu-id="37f82-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="37f82-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37f82-132">-Confirm</span></span>
<span data-ttu-id="37f82-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37f82-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37f82-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37f82-134">-WhatIf</span></span>
<span data-ttu-id="37f82-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37f82-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37f82-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37f82-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37f82-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f82-137">CommonParameters</span></span>
<span data-ttu-id="37f82-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37f82-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f82-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37f82-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f82-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="37f82-140">INPUTS</span></span>

### <span data-ttu-id="37f82-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="37f82-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="37f82-142">System.String</span><span class="sxs-lookup"><span data-stu-id="37f82-142">System.String</span></span>

## <span data-ttu-id="37f82-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37f82-143">OUTPUTS</span></span>

### <span data-ttu-id="37f82-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="37f82-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="37f82-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="37f82-145">NOTES</span></span>

## <span data-ttu-id="37f82-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37f82-146">RELATED LINKS</span></span>
