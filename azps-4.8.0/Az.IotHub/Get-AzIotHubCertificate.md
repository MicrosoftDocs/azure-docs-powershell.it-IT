---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 8bc586ea9543c7545e7d24e3bc6d7bc36bb77d49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190696"
---
# <span data-ttu-id="e2af4-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="e2af4-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="e2af4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2af4-102">SYNOPSIS</span></span>
<span data-ttu-id="e2af4-103">Elenca tutti i certificati o un determinato certificato contenuto in un hub di Azure.</span><span class="sxs-lookup"><span data-stu-id="e2af4-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="e2af4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2af4-104">SYNTAX</span></span>

### <span data-ttu-id="e2af4-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2af4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2af4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e2af4-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2af4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e2af4-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2af4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2af4-108">DESCRIPTION</span></span>
<span data-ttu-id="e2af4-109">Per una spiegazione dettagliata dei certificati della CA in Azure molto Hub, vedere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="e2af4-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="e2af4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2af4-110">EXAMPLES</span></span>

### <span data-ttu-id="e2af4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e2af4-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="e2af4-112">Elenca tutti i certificati in MyIotHub</span><span class="sxs-lookup"><span data-stu-id="e2af4-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="e2af4-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e2af4-113">Example 2</span></span>
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

<span data-ttu-id="e2af4-114">Visualizzare i dettagli relativi a un certificato</span><span class="sxs-lookup"><span data-stu-id="e2af4-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="e2af4-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2af4-115">PARAMETERS</span></span>

### <span data-ttu-id="e2af4-116">-Certificate</span><span class="sxs-lookup"><span data-stu-id="e2af4-116">-CertificateName</span></span>
<span data-ttu-id="e2af4-117">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="e2af4-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="e2af4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2af4-118">-DefaultProfile</span></span>
<span data-ttu-id="e2af4-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2af4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2af4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2af4-120">-InputObject</span></span>
<span data-ttu-id="e2af4-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="e2af4-121">IotHub Object</span></span>

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

### <span data-ttu-id="e2af4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2af4-122">-Name</span></span>
<span data-ttu-id="e2af4-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="e2af4-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e2af4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2af4-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2af4-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e2af4-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e2af4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2af4-126">-ResourceId</span></span>
<span data-ttu-id="e2af4-127">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="e2af4-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e2af4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2af4-128">CommonParameters</span></span>
<span data-ttu-id="e2af4-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2af4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2af4-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2af4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2af4-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2af4-131">INPUTS</span></span>

### <span data-ttu-id="e2af4-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e2af4-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e2af4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e2af4-133">System.String</span></span>

## <span data-ttu-id="e2af4-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2af4-134">OUTPUTS</span></span>

### <span data-ttu-id="e2af4-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="e2af4-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="e2af4-136">Note</span><span class="sxs-lookup"><span data-stu-id="e2af4-136">NOTES</span></span>

## <span data-ttu-id="e2af4-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2af4-137">RELATED LINKS</span></span>
