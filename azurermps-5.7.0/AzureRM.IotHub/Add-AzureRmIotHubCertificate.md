---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubCertificate.md
ms.openlocfilehash: b38fd64db24a38267b3d06d8046f1bcbb826537f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686515"
---
# <span data-ttu-id="87c90-101">Add-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="87c90-101">Add-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="87c90-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87c90-102">SYNOPSIS</span></span>
<span data-ttu-id="87c90-103">Creare/aggiornare un certificato Hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="87c90-103">Create/update an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87c90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87c90-104">SYNTAX</span></span>

### <span data-ttu-id="87c90-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="87c90-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87c90-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="87c90-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87c90-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="87c90-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87c90-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87c90-108">DESCRIPTION</span></span>
<span data-ttu-id="87c90-109">Carica un nuovo certificato o sostituisce il certificato esistente con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="87c90-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="87c90-110">Per una spiegazione dettagliata dei certificati della CA in Azure molto Hub, vedere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="87c90-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="87c90-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87c90-111">EXAMPLES</span></span>

### <span data-ttu-id="87c90-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="87c90-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="87c90-113">Carica un file CER certificato CA in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="87c90-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="87c90-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="87c90-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="87c90-115">Aggiorna un certificato CA in un hub di un sacco caricando un nuovo file CER.</span><span class="sxs-lookup"><span data-stu-id="87c90-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="87c90-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87c90-116">PARAMETERS</span></span>

### <span data-ttu-id="87c90-117">-Certificate</span><span class="sxs-lookup"><span data-stu-id="87c90-117">-CertificateName</span></span>
<span data-ttu-id="87c90-118">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="87c90-118">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c90-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c90-119">-DefaultProfile</span></span>
<span data-ttu-id="87c90-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87c90-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87c90-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="87c90-121">-Etag</span></span>
<span data-ttu-id="87c90-122">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="87c90-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="87c90-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87c90-123">-InputObject</span></span>
<span data-ttu-id="87c90-124">Oggetto certificato</span><span class="sxs-lookup"><span data-stu-id="87c90-124">Certificate Object</span></span>

```yaml
Type: PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87c90-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="87c90-125">-Name</span></span>
<span data-ttu-id="87c90-126">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="87c90-126">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c90-127">-Path</span><span class="sxs-lookup"><span data-stu-id="87c90-127">-Path</span></span>
<span data-ttu-id="87c90-128">rappresentazione di base-64 del file certificato. cer di X509 o del percorso di file con estensione PEM.</span><span class="sxs-lookup"><span data-stu-id="87c90-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="87c90-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87c90-129">-ResourceGroupName</span></span>
<span data-ttu-id="87c90-130">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="87c90-130">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c90-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87c90-131">-ResourceId</span></span>
<span data-ttu-id="87c90-132">ID risorsa certificato</span><span class="sxs-lookup"><span data-stu-id="87c90-132">Certificate Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c90-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="87c90-133">-Confirm</span></span>
<span data-ttu-id="87c90-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87c90-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c90-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87c90-135">-WhatIf</span></span>
<span data-ttu-id="87c90-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="87c90-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87c90-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="87c90-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c90-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c90-138">CommonParameters</span></span>
<span data-ttu-id="87c90-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87c90-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c90-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87c90-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c90-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87c90-141">INPUTS</span></span>

### <span data-ttu-id="87c90-142">System. String</span><span class="sxs-lookup"><span data-stu-id="87c90-142">System.String</span></span>

## <span data-ttu-id="87c90-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87c90-143">OUTPUTS</span></span>

### <span data-ttu-id="87c90-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="87c90-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="87c90-145">Note</span><span class="sxs-lookup"><span data-stu-id="87c90-145">NOTES</span></span>

## <span data-ttu-id="87c90-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87c90-146">RELATED LINKS</span></span>

