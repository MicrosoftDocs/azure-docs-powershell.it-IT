---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 517f4822817a97c6ac22facb206b513a06f85d6d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861406"
---
# <span data-ttu-id="cf364-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="cf364-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="cf364-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf364-102">SYNOPSIS</span></span>
<span data-ttu-id="cf364-103">Elenca tutti i certificati o un determinato certificato contenuto in un hub di Azure.</span><span class="sxs-lookup"><span data-stu-id="cf364-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="cf364-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf364-104">SYNTAX</span></span>

### <span data-ttu-id="cf364-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf364-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf364-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cf364-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf364-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cf364-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf364-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf364-108">DESCRIPTION</span></span>
<span data-ttu-id="cf364-109">Per una spiegazione dettagliata dei certificati della CA in Azure molto Hub, vedere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="cf364-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="cf364-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf364-110">EXAMPLES</span></span>

### <span data-ttu-id="cf364-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cf364-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="cf364-112">Elenca tutti i certificati in MyIotHub</span><span class="sxs-lookup"><span data-stu-id="cf364-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="cf364-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cf364-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

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

<span data-ttu-id="cf364-114">Visualizzare i dettagli relativi a un certificato</span><span class="sxs-lookup"><span data-stu-id="cf364-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="cf364-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf364-115">PARAMETERS</span></span>

### <span data-ttu-id="cf364-116">-Certificate</span><span class="sxs-lookup"><span data-stu-id="cf364-116">-CertificateName</span></span>
<span data-ttu-id="cf364-117">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="cf364-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="cf364-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf364-118">-DefaultProfile</span></span>
<span data-ttu-id="cf364-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf364-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf364-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf364-120">-InputObject</span></span>
<span data-ttu-id="cf364-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="cf364-121">IotHub Object</span></span>

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

### <span data-ttu-id="cf364-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf364-122">-Name</span></span>
<span data-ttu-id="cf364-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="cf364-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cf364-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf364-124">-ResourceGroupName</span></span>
<span data-ttu-id="cf364-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="cf364-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cf364-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf364-126">-ResourceId</span></span>
<span data-ttu-id="cf364-127">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="cf364-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cf364-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf364-128">CommonParameters</span></span>
<span data-ttu-id="cf364-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf364-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf364-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf364-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf364-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf364-131">INPUTS</span></span>

### <span data-ttu-id="cf364-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cf364-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cf364-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cf364-133">System.String</span></span>

## <span data-ttu-id="cf364-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf364-134">OUTPUTS</span></span>

### <span data-ttu-id="cf364-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="cf364-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="cf364-136">Note</span><span class="sxs-lookup"><span data-stu-id="cf364-136">NOTES</span></span>

## <span data-ttu-id="cf364-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf364-137">RELATED LINKS</span></span>
