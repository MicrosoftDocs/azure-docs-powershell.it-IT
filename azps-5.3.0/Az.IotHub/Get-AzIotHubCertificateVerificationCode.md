---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 4bf362402ba3db0ba50d9144d6bb9fa79977a998
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487099"
---
# <span data-ttu-id="2351d-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="2351d-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="2351d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2351d-102">SYNOPSIS</span></span>
<span data-ttu-id="2351d-103">Genera un codice di verifica per un certificato Hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="2351d-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="2351d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2351d-104">SYNTAX</span></span>

### <span data-ttu-id="2351d-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2351d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2351d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2351d-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2351d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2351d-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2351d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2351d-108">DESCRIPTION</span></span>
<span data-ttu-id="2351d-109">Questo codice di verifica viene usato per completare il passaggio della prova del possesso per un certificato.</span><span class="sxs-lookup"><span data-stu-id="2351d-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="2351d-110">Usare questo codice di verifica come CN di un nuovo certificato firmato con la chiave privata certificati radice.</span><span class="sxs-lookup"><span data-stu-id="2351d-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="2351d-111">Per una spiegazione dettagliata dei certificati della CA in Azure molto Hub, vedere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="2351d-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="2351d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2351d-112">EXAMPLES</span></span>

### <span data-ttu-id="2351d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2351d-113">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
VerificationCode    : 47292AB6260DB02CCD2D07C601B7303DD49858B6
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="2351d-114">Genera un codice di verifica per il certificato</span><span class="sxs-lookup"><span data-stu-id="2351d-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="2351d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2351d-115">PARAMETERS</span></span>

### <span data-ttu-id="2351d-116">-Certificate</span><span class="sxs-lookup"><span data-stu-id="2351d-116">-CertificateName</span></span>
<span data-ttu-id="2351d-117">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="2351d-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="2351d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2351d-118">-DefaultProfile</span></span>
<span data-ttu-id="2351d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2351d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2351d-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="2351d-120">-Etag</span></span>
<span data-ttu-id="2351d-121">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="2351d-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="2351d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2351d-122">-InputObject</span></span>
<span data-ttu-id="2351d-123">Oggetto certificato</span><span class="sxs-lookup"><span data-stu-id="2351d-123">Certificate Object</span></span>

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

### <span data-ttu-id="2351d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="2351d-124">-Name</span></span>
<span data-ttu-id="2351d-125">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="2351d-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2351d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2351d-126">-ResourceGroupName</span></span>
<span data-ttu-id="2351d-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2351d-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2351d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2351d-128">-ResourceId</span></span>
<span data-ttu-id="2351d-129">ID risorsa certificato</span><span class="sxs-lookup"><span data-stu-id="2351d-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="2351d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2351d-130">CommonParameters</span></span>
<span data-ttu-id="2351d-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2351d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2351d-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2351d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2351d-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2351d-133">INPUTS</span></span>

### <span data-ttu-id="2351d-134">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="2351d-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="2351d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2351d-135">System.String</span></span>

## <span data-ttu-id="2351d-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2351d-136">OUTPUTS</span></span>

### <span data-ttu-id="2351d-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="2351d-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="2351d-138">Note</span><span class="sxs-lookup"><span data-stu-id="2351d-138">NOTES</span></span>

## <span data-ttu-id="2351d-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2351d-139">RELATED LINKS</span></span>
