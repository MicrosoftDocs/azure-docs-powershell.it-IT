---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnetworkstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
ms.openlocfilehash: 5ba351ab1a5102acc1855e13821650b8ce1b4373
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302208"
---
# <span data-ttu-id="9103e-101">Get-AzApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="9103e-101">Get-AzApiManagementNetworkStatus</span></span>

## <span data-ttu-id="9103e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9103e-102">SYNOPSIS</span></span>
<span data-ttu-id="9103e-103">Ottiene lo stato di connettività per le risorse esterne in cui il servizio di gestione API dipende dall'interno del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="9103e-103">Gets the Connectivity Status to the external resources on which the Api Management service depends from inside the Cloud Service.</span></span> <span data-ttu-id="9103e-104">Questo restituisce anche i server DNS come visibili a CloudService.</span><span class="sxs-lookup"><span data-stu-id="9103e-104">This also returns the DNS Servers as visible to the CloudService.</span></span>

## <span data-ttu-id="9103e-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9103e-105">SYNTAX</span></span>

### <span data-ttu-id="9103e-106">ByInputObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9103e-106">ByInputObject (Default)</span></span>
```
Get-AzApiManagementNetworkStatus -ApiManagementObject <PsApiManagement> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9103e-107">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="9103e-107">ExpandedParameter</span></span>
```
Get-AzApiManagementNetworkStatus -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9103e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9103e-108">DESCRIPTION</span></span>
<span data-ttu-id="9103e-109">Ottiene lo stato della rete del servizio di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="9103e-109">Gets the Network status of their Api Management service</span></span>

## <span data-ttu-id="9103e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9103e-110">EXAMPLES</span></span>

### <span data-ttu-id="9103e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9103e-111">Example 1</span></span>
```powershell
PS D:\github\azure-powershell> Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice

Location DnsServers      ConnectivityStatus
-------- ----------      ------------------
West US  {168.63.129.16} {apimgmtstaoonqs7wwzjosky.blob.core.windows.net, apimgmtstaoonqs7wwzjosky.file.core.windows.net, apimgmtstaoonqs7wwzjosky.queue.core.windows.net, apimgmtstaoonqs7wwzjosk...


PS D:\github\azure-powershell> $networkStatus = Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice
PS D:\github\azure-powershell> $networkStatus.ConnectivityStatus


Name             : apimgmtstaoonqs7wwzjosky.blob.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : apimgmtstaoonqs7wwzjosky.file.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.queue.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.table.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : bx9gltecfv.database.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:41 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : https://prod3.metrics.nsatc.net:1886/RecoveryService
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:07:11 PM
LastStatusChange : 4/29/2019 1:31:30 PM

Name             : prod.warmpath.msftcloudes.com
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : Scm
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:04:27 PM
LastStatusChange : 4/30/2019 11:16:20 PM
```

<span data-ttu-id="9103e-112">Ottiene lo stato di connettività delle diverse risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9103e-112">Gets the connectivity status of the different resources on which ApiManagement service depends upon.</span></span>

## <span data-ttu-id="9103e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9103e-113">PARAMETERS</span></span>

### <span data-ttu-id="9103e-114">-ApiManagementObject</span><span class="sxs-lookup"><span data-stu-id="9103e-114">-ApiManagementObject</span></span>
<span data-ttu-id="9103e-115">Istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9103e-115">Instance of PsApiManagement.</span></span> <span data-ttu-id="9103e-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9103e-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9103e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9103e-117">-DefaultProfile</span></span>
<span data-ttu-id="9103e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9103e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9103e-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9103e-119">-Location</span></span>
<span data-ttu-id="9103e-120">Posizione del servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="9103e-120">Location of the API Management Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9103e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9103e-121">-Name</span></span>
<span data-ttu-id="9103e-122">Nome della gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="9103e-122">Name of API Management.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9103e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9103e-123">-ResourceGroupName</span></span>
<span data-ttu-id="9103e-124">Nome del gruppo di risorse in cui è presente la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="9103e-124">Name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9103e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9103e-125">CommonParameters</span></span>
<span data-ttu-id="9103e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9103e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9103e-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9103e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9103e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9103e-128">INPUTS</span></span>

### <span data-ttu-id="9103e-129">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9103e-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="9103e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9103e-130">System.String</span></span>

## <span data-ttu-id="9103e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9103e-131">OUTPUTS</span></span>

### <span data-ttu-id="9103e-132">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="9103e-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementNetworkStatus</span></span>

## <span data-ttu-id="9103e-133">Note</span><span class="sxs-lookup"><span data-stu-id="9103e-133">NOTES</span></span>

## <span data-ttu-id="9103e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9103e-134">RELATED LINKS</span></span>
