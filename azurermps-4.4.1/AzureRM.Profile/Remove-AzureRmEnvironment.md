---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: d27a05e652cbcd11d35536ebff97f04b3c60f520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688264"
---
# <span data-ttu-id="a66d3-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="a66d3-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="a66d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a66d3-102">SYNOPSIS</span></span>
<span data-ttu-id="a66d3-103">Rimuove gli endpoint e i metadati per la connessione a una determinata istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="a66d3-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a66d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a66d3-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a66d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a66d3-105">DESCRIPTION</span></span>
<span data-ttu-id="a66d3-106">Il cmdlet Remove-AzureRmEnvironment rimuove gli endpoint e le informazioni sui metadati per la connessione a una determinata istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="a66d3-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="a66d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a66d3-107">EXAMPLES</span></span>

### <span data-ttu-id="a66d3-108">Esempio 1: creazione e rimozione di un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="a66d3-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="a66d3-109">Questo esempio Mostra come creare un ambiente usando Add-AzureRmEnvironment e quindi come eliminare l'ambiente tramite Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="a66d3-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="a66d3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a66d3-110">PARAMETERS</span></span>

### <span data-ttu-id="a66d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a66d3-111">-DefaultProfile</span></span>
<span data-ttu-id="a66d3-112">Le credenziali, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a66d3-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a66d3-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a66d3-113">-Name</span></span>
<span data-ttu-id="a66d3-114">Specifica il nome dell'ambiente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a66d3-114">Specifies the name of the environment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a66d3-115">-Ambito</span><span class="sxs-lookup"><span data-stu-id="a66d3-115">-Scope</span></span>
<span data-ttu-id="a66d3-116">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="a66d3-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66d3-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a66d3-117">-Confirm</span></span>
<span data-ttu-id="a66d3-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a66d3-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66d3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a66d3-119">-WhatIf</span></span>
<span data-ttu-id="a66d3-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a66d3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a66d3-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a66d3-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66d3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a66d3-122">CommonParameters</span></span>
<span data-ttu-id="a66d3-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a66d3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a66d3-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a66d3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a66d3-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a66d3-125">INPUTS</span></span>

## <span data-ttu-id="a66d3-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a66d3-126">OUTPUTS</span></span>

### <span data-ttu-id="a66d3-127">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a66d3-127">PSAzureEnvironment</span></span>

## <span data-ttu-id="a66d3-128">Note</span><span class="sxs-lookup"><span data-stu-id="a66d3-128">NOTES</span></span>

## <span data-ttu-id="a66d3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a66d3-129">RELATED LINKS</span></span>

[<span data-ttu-id="a66d3-130">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="a66d3-130">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="a66d3-131">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="a66d3-131">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="a66d3-132">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="a66d3-132">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

