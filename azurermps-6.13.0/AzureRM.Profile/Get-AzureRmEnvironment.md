---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
ms.openlocfilehash: ef42490d18702682413fd2c0a19e301614ce4d94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514948"
---
# <span data-ttu-id="42978-101">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="42978-101">Get-AzureRmEnvironment</span></span>

## <span data-ttu-id="42978-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42978-102">SYNOPSIS</span></span>
<span data-ttu-id="42978-103">Ottenere endpoint e metadati per un'istanza di Azure Services.</span><span class="sxs-lookup"><span data-stu-id="42978-103">Get endpoints and metadata for an instance of Azure services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42978-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42978-104">SYNTAX</span></span>

```
Get-AzureRmEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42978-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42978-105">DESCRIPTION</span></span>
<span data-ttu-id="42978-106">Il cmdlet Get-AzureRmEnvironment ottiene gli endpoint e i metadati per un'istanza di Azure Services.</span><span class="sxs-lookup"><span data-stu-id="42978-106">The Get-AzureRmEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="42978-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42978-107">EXAMPLES</span></span>

### <span data-ttu-id="42978-108">Esempio 1: recupero dell'ambiente AzureCloud</span><span class="sxs-lookup"><span data-stu-id="42978-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="42978-109">Questo esempio Mostra come ottenere gli endpoint e i metadati per l'ambiente AzureCloud (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="42978-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="42978-110">Esempio 2: recupero dell'ambiente AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="42978-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301776
ResourceManagerUrl                                : https://management.chinacloudapi.cn/
SqlDatabaseDnsSuffix                              : .database.chinacloudapi.cn
StorageEndpointSuffix                             : core.chinacloudapi.cn
ActiveDirectoryAuthority                          : https://login.chinacloudapi.cn/
GraphUrl                                          : https://graph.chinacloudapi.cn/
GraphEndpointResourceId                           : https://graph.chinacloudapi.cn/
TrafficManagerDnsSuffix                           : trafficmanager.cn
AzureKeyVaultDnsSuffix                            : vault.azure.cn
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.cn
```

<span data-ttu-id="42978-111">Questo esempio Mostra come ottenere gli endpoint e i metadati per l'ambiente AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="42978-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="42978-112">Esempio 3: recupero dell'ambiente AzureUSGovernment</span><span class="sxs-lookup"><span data-stu-id="42978-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="42978-113">Questo esempio Mostra come ottenere gli endpoint e i metadati per l'ambiente AzureUSGovernment.</span><span class="sxs-lookup"><span data-stu-id="42978-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="42978-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42978-114">PARAMETERS</span></span>

### <span data-ttu-id="42978-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42978-115">-DefaultProfile</span></span>
<span data-ttu-id="42978-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42978-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42978-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="42978-117">-Name</span></span>
<span data-ttu-id="42978-118">Specifica il nome dell'istanza di Azure da ottenere.</span><span class="sxs-lookup"><span data-stu-id="42978-118">Specifies the name of the Azure instance to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42978-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42978-119">CommonParameters</span></span>
<span data-ttu-id="42978-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42978-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42978-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42978-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42978-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42978-122">INPUTS</span></span>

### <span data-ttu-id="42978-123">System. String</span><span class="sxs-lookup"><span data-stu-id="42978-123">System.String</span></span>

## <span data-ttu-id="42978-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42978-124">OUTPUTS</span></span>

### <span data-ttu-id="42978-125">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="42978-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="42978-126">Note</span><span class="sxs-lookup"><span data-stu-id="42978-126">NOTES</span></span>

## <span data-ttu-id="42978-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42978-127">RELATED LINKS</span></span>

[<span data-ttu-id="42978-128">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="42978-128">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="42978-129">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="42978-129">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="42978-130">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="42978-130">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

