---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
ms.openlocfilehash: 55cd14216e9a592128c8d600238b49862cb1f20a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515691"
---
# <span data-ttu-id="4e1fe-101">Get-AzureRmIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="4e1fe-101">Get-AzureRmIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="4e1fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="4e1fe-103">Genera un codice di verifica per un certificato Hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e1fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e1fe-104">SYNTAX</span></span>

### <span data-ttu-id="4e1fe-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4e1fe-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e1fe-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4e1fe-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e1fe-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4e1fe-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e1fe-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e1fe-108">DESCRIPTION</span></span>
<span data-ttu-id="4e1fe-109">Questo codice di verifica viene usato per completare il passaggio della prova del possesso per un certificato.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="4e1fe-110">Usare questo codice di verifica come CN di un nuovo certificato firmato con la chiave privata certificati radice.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="4e1fe-111">Per una spiegazione dettagliata dei certificati della CA in Azure molto Hub, vedere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="4e1fe-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="4e1fe-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e1fe-112">EXAMPLES</span></span>

### <span data-ttu-id="4e1fe-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e1fe-113">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="4e1fe-114">Genera un codice di verifica per il certificato</span><span class="sxs-lookup"><span data-stu-id="4e1fe-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="4e1fe-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e1fe-115">PARAMETERS</span></span>

### <span data-ttu-id="4e1fe-116">-Certificate</span><span class="sxs-lookup"><span data-stu-id="4e1fe-116">-CertificateName</span></span>
<span data-ttu-id="4e1fe-117">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="4e1fe-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="4e1fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e1fe-118">-DefaultProfile</span></span>
<span data-ttu-id="4e1fe-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e1fe-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="4e1fe-120">-Etag</span></span>
<span data-ttu-id="4e1fe-121">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="4e1fe-121">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1fe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e1fe-122">-InputObject</span></span>
<span data-ttu-id="4e1fe-123">Oggetto certificato</span><span class="sxs-lookup"><span data-stu-id="4e1fe-123">Certificate Object</span></span>

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

### <span data-ttu-id="4e1fe-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e1fe-124">-Name</span></span>
<span data-ttu-id="4e1fe-125">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="4e1fe-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4e1fe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e1fe-126">-ResourceGroupName</span></span>
<span data-ttu-id="4e1fe-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4e1fe-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4e1fe-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e1fe-128">-ResourceId</span></span>
<span data-ttu-id="4e1fe-129">ID risorsa certificato</span><span class="sxs-lookup"><span data-stu-id="4e1fe-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="4e1fe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e1fe-130">CommonParameters</span></span>
<span data-ttu-id="4e1fe-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e1fe-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e1fe-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e1fe-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e1fe-133">INPUTS</span></span>

### <span data-ttu-id="4e1fe-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4e1fe-134">System.String</span></span>

## <span data-ttu-id="4e1fe-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e1fe-135">OUTPUTS</span></span>

### <span data-ttu-id="4e1fe-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="4e1fe-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="4e1fe-137">Note</span><span class="sxs-lookup"><span data-stu-id="4e1fe-137">NOTES</span></span>

## <span data-ttu-id="4e1fe-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e1fe-138">RELATED LINKS</span></span>
