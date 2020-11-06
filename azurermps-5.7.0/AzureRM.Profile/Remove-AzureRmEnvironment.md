---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: 2916a4048987d703bc1cbb44653eae2cfb066a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520425"
---
# <span data-ttu-id="1f184-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="1f184-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="1f184-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f184-102">SYNOPSIS</span></span>
<span data-ttu-id="1f184-103">Rimuove gli endpoint e i metadati per la connessione a una determinata istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f184-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f184-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f184-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f184-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f184-105">DESCRIPTION</span></span>
<span data-ttu-id="1f184-106">Il cmdlet Remove-AzureRmEnvironment rimuove gli endpoint e le informazioni sui metadati per la connessione a una determinata istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f184-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="1f184-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f184-107">EXAMPLES</span></span>

### <span data-ttu-id="1f184-108">Esempio 1: creazione e rimozione di un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="1f184-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="1f184-109">Questo esempio Mostra come creare un ambiente usando Add-AzureRmEnvironment e quindi come eliminare l'ambiente tramite Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="1f184-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="1f184-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f184-110">PARAMETERS</span></span>

### <span data-ttu-id="1f184-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f184-111">-DefaultProfile</span></span>
<span data-ttu-id="1f184-112">Le credenziali, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f184-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f184-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f184-113">-Name</span></span>
<span data-ttu-id="1f184-114">Specifica il nome dell'ambiente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1f184-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="1f184-115">-Ambito</span><span class="sxs-lookup"><span data-stu-id="1f184-115">-Scope</span></span>
<span data-ttu-id="1f184-116">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="1f184-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f184-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f184-117">-Confirm</span></span>
<span data-ttu-id="1f184-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f184-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f184-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f184-119">-WhatIf</span></span>
<span data-ttu-id="1f184-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f184-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f184-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f184-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f184-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f184-122">CommonParameters</span></span>
<span data-ttu-id="1f184-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f184-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f184-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f184-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f184-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f184-125">INPUTS</span></span>

### <span data-ttu-id="1f184-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1f184-126">None</span></span>
<span data-ttu-id="1f184-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1f184-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f184-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f184-128">OUTPUTS</span></span>

### <span data-ttu-id="1f184-129">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="1f184-129">PSAzureEnvironment</span></span>

## <span data-ttu-id="1f184-130">Note</span><span class="sxs-lookup"><span data-stu-id="1f184-130">NOTES</span></span>

## <span data-ttu-id="1f184-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f184-131">RELATED LINKS</span></span>

[<span data-ttu-id="1f184-132">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="1f184-132">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="1f184-133">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="1f184-133">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="1f184-134">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="1f184-134">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

