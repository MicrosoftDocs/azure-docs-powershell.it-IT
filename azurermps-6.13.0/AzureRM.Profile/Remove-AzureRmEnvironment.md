---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: 05a4b2a475b2bd58de706ba038f2760d133b7dbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517356"
---
# <span data-ttu-id="cb4f5-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="cb4f5-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="cb4f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb4f5-102">SYNOPSIS</span></span>
<span data-ttu-id="cb4f5-103">Rimuove gli endpoint e i metadati per la connessione a una determinata istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb4f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb4f5-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb4f5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb4f5-105">DESCRIPTION</span></span>
<span data-ttu-id="cb4f5-106">Il cmdlet Remove-AzureRmEnvironment rimuove gli endpoint e le informazioni sui metadati per la connessione a una determinata istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="cb4f5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb4f5-107">EXAMPLES</span></span>

### <span data-ttu-id="cb4f5-108">Esempio 1: creazione e rimozione di un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="cb4f5-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="cb4f5-109">Questo esempio Mostra come creare un ambiente usando Add-AzureRmEnvironment e quindi come eliminare l'ambiente tramite Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="cb4f5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb4f5-110">PARAMETERS</span></span>

### <span data-ttu-id="cb4f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb4f5-111">-DefaultProfile</span></span>
<span data-ttu-id="cb4f5-112">Le credenziali, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb4f5-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb4f5-113">-Name</span></span>
<span data-ttu-id="cb4f5-114">Specifica il nome dell'ambiente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="cb4f5-115">-Ambito</span><span class="sxs-lookup"><span data-stu-id="cb4f5-115">-Scope</span></span>
<span data-ttu-id="cb4f5-116">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="cb4f5-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cb4f5-117">-Confirm</span></span>
<span data-ttu-id="cb4f5-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb4f5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb4f5-119">-WhatIf</span></span>
<span data-ttu-id="cb4f5-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb4f5-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb4f5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb4f5-122">CommonParameters</span></span>
<span data-ttu-id="cb4f5-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb4f5-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb4f5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb4f5-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb4f5-125">INPUTS</span></span>

### <span data-ttu-id="cb4f5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cb4f5-126">System.String</span></span>

## <span data-ttu-id="cb4f5-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb4f5-127">OUTPUTS</span></span>

### <span data-ttu-id="cb4f5-128">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="cb4f5-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="cb4f5-129">Note</span><span class="sxs-lookup"><span data-stu-id="cb4f5-129">NOTES</span></span>

## <span data-ttu-id="cb4f5-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb4f5-130">RELATED LINKS</span></span>

[<span data-ttu-id="cb4f5-131">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="cb4f5-131">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="cb4f5-132">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="cb4f5-132">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="cb4f5-133">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="cb4f5-133">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

