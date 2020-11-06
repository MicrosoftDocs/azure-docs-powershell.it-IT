---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificate.md
ms.openlocfilehash: 745fcb6fdfb9ee47faf28cde84985dcfd7199ecc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520998"
---
# <span data-ttu-id="b0d5d-101">Get-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="b0d5d-101">Get-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="b0d5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d5d-103">Elenca tutti i certificati o un determinato certificato contenuto in un hub di Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d5d-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0d5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0d5d-104">SYNTAX</span></span>

### <span data-ttu-id="b0d5d-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0d5d-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0d5d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b0d5d-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0d5d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b0d5d-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0d5d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0d5d-108">DESCRIPTION</span></span>
<span data-ttu-id="b0d5d-109">Per una spiegazione dettagliata dei certificati della CA in Azure molto Hub, vedere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="b0d5d-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="b0d5d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0d5d-110">EXAMPLES</span></span>

### <span data-ttu-id="b0d5d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b0d5d-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="b0d5d-112">Elenca tutti i certificati in MyIotHub</span><span class="sxs-lookup"><span data-stu-id="b0d5d-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="b0d5d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b0d5d-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

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

<span data-ttu-id="b0d5d-114">Visualizzare i dettagli relativi a un certificato</span><span class="sxs-lookup"><span data-stu-id="b0d5d-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="b0d5d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0d5d-115">PARAMETERS</span></span>

### <span data-ttu-id="b0d5d-116">-Certificate</span><span class="sxs-lookup"><span data-stu-id="b0d5d-116">-CertificateName</span></span>
<span data-ttu-id="b0d5d-117">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="b0d5d-117">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0d5d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d5d-118">-DefaultProfile</span></span>
<span data-ttu-id="b0d5d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d5d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0d5d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0d5d-120">-InputObject</span></span>
<span data-ttu-id="b0d5d-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="b0d5d-121">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0d5d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0d5d-122">-Name</span></span>
<span data-ttu-id="b0d5d-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="b0d5d-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0d5d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0d5d-124">-ResourceGroupName</span></span>
<span data-ttu-id="b0d5d-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b0d5d-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b0d5d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0d5d-126">-ResourceId</span></span>
<span data-ttu-id="b0d5d-127">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="b0d5d-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b0d5d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d5d-128">CommonParameters</span></span>
<span data-ttu-id="b0d5d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d5d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d5d-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0d5d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d5d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0d5d-131">INPUTS</span></span>

### <span data-ttu-id="b0d5d-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b0d5d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="b0d5d-133">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b0d5d-133">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="b0d5d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b0d5d-134">System.String</span></span>

## <span data-ttu-id="b0d5d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0d5d-135">OUTPUTS</span></span>

### <span data-ttu-id="b0d5d-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="b0d5d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="b0d5d-137">Note</span><span class="sxs-lookup"><span data-stu-id="b0d5d-137">NOTES</span></span>

## <span data-ttu-id="b0d5d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0d5d-138">RELATED LINKS</span></span>
