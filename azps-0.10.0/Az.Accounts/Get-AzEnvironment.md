---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: 27407977551f1124be9040555336e4d6bc4d73e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860218"
---
# <span data-ttu-id="e29ce-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e29ce-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="e29ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e29ce-102">SYNOPSIS</span></span>
<span data-ttu-id="e29ce-103">Ottenere endpoint e metadati per un'istanza di Azure Services.</span><span class="sxs-lookup"><span data-stu-id="e29ce-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="e29ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e29ce-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e29ce-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e29ce-105">DESCRIPTION</span></span>
<span data-ttu-id="e29ce-106">Il cmdlet Get-AzEnvironment ottiene gli endpoint e i metadati per un'istanza di Azure Services.</span><span class="sxs-lookup"><span data-stu-id="e29ce-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="e29ce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e29ce-107">EXAMPLES</span></span>

### <span data-ttu-id="e29ce-108">Esempio 1: recupero dell'ambiente AzureCloud</span><span class="sxs-lookup"><span data-stu-id="e29ce-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="e29ce-109">Questo esempio Mostra come ottenere gli endpoint e i metadati per l'ambiente AzureCloud (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="e29ce-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="e29ce-110">Esempio 2: recupero dell'ambiente AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="e29ce-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : http://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : http://go.microsoft.com/fwlink/?LinkID=301776
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

<span data-ttu-id="e29ce-111">Questo esempio Mostra come ottenere gli endpoint e i metadati per l'ambiente AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="e29ce-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="e29ce-112">Esempio 3: recupero dell'ambiente AzureUSGovernment</span><span class="sxs-lookup"><span data-stu-id="e29ce-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="e29ce-113">Questo esempio Mostra come ottenere gli endpoint e i metadati per l'ambiente AzureUSGovernment.</span><span class="sxs-lookup"><span data-stu-id="e29ce-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="e29ce-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e29ce-114">PARAMETERS</span></span>

### <span data-ttu-id="e29ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e29ce-115">-DefaultProfile</span></span>
<span data-ttu-id="e29ce-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e29ce-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e29ce-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e29ce-117">-Name</span></span>
<span data-ttu-id="e29ce-118">Specifica il nome dell'istanza di Azure da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e29ce-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="e29ce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29ce-119">CommonParameters</span></span>
<span data-ttu-id="e29ce-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e29ce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29ce-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e29ce-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29ce-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e29ce-122">INPUTS</span></span>

### <span data-ttu-id="e29ce-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e29ce-123">System.String</span></span>

## <span data-ttu-id="e29ce-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e29ce-124">OUTPUTS</span></span>

### <span data-ttu-id="e29ce-125">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e29ce-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="e29ce-126">Note</span><span class="sxs-lookup"><span data-stu-id="e29ce-126">NOTES</span></span>

## <span data-ttu-id="e29ce-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e29ce-127">RELATED LINKS</span></span>

[<span data-ttu-id="e29ce-128">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e29ce-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="e29ce-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e29ce-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="e29ce-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e29ce-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

