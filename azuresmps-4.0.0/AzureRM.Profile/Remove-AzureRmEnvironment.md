---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d9c783d6fe4047aa1d179cd661c88d13e9c716b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685212"
---
# <span data-ttu-id="af7f1-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="af7f1-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="af7f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af7f1-102">SYNOPSIS</span></span>
<span data-ttu-id="af7f1-103">Rimuove gli endpoint e i metadati per la connessione a una determinata istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="af7f1-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="af7f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af7f1-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af7f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af7f1-105">DESCRIPTION</span></span>
<span data-ttu-id="af7f1-106">Il cmdlet Remove-AzureRmEnvironment rimuove gli endpoint e le informazioni sui metadati per la connessione a una determinata istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="af7f1-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="af7f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af7f1-107">EXAMPLES</span></span>

### <span data-ttu-id="af7f1-108">Esempio 1: creazione e rimozione di un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="af7f1-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
```

<span data-ttu-id="af7f1-109">Questo esempio Mostra come creare un ambiente usando Add-AzureRmEnvironment e quindi come eliminare l'ambiente tramite Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="af7f1-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="af7f1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af7f1-110">PARAMETERS</span></span>

### <span data-ttu-id="af7f1-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="af7f1-111">-Name</span></span>
<span data-ttu-id="af7f1-112">Specifica il nome dell'ambiente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="af7f1-112">Specifies the name of the environment to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af7f1-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af7f1-113">-Confirm</span></span>
<span data-ttu-id="af7f1-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af7f1-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af7f1-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af7f1-115">-WhatIf</span></span>
<span data-ttu-id="af7f1-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af7f1-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af7f1-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af7f1-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af7f1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7f1-118">CommonParameters</span></span>
<span data-ttu-id="af7f1-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af7f1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7f1-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af7f1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7f1-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af7f1-121">INPUTS</span></span>

## <span data-ttu-id="af7f1-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af7f1-122">OUTPUTS</span></span>

### <span data-ttu-id="af7f1-123">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="af7f1-123">PSAzureEnvironment</span></span>

## <span data-ttu-id="af7f1-124">Note</span><span class="sxs-lookup"><span data-stu-id="af7f1-124">NOTES</span></span>

## <span data-ttu-id="af7f1-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af7f1-125">RELATED LINKS</span></span>

[<span data-ttu-id="af7f1-126">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="af7f1-126">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="af7f1-127">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="af7f1-127">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="af7f1-128">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="af7f1-128">Set-AzureRMEnvironment</span></span>]()

