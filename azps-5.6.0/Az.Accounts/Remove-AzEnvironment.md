---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 5acba21e8daf1adaa83820d67c5955b27230c4ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954910"
---
# <span data-ttu-id="05869-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="05869-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="05869-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05869-102">SYNOPSIS</span></span>
<span data-ttu-id="05869-103">Rimuove gli endpoint e i metadati per la connessione a una determinata istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="05869-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="05869-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05869-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05869-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="05869-105">DESCRIPTION</span></span>
<span data-ttu-id="05869-106">Il cmdlet Remove-AzEnvironment rimuove gli endpoint e le informazioni sui metadati per la connessione a una determinata istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="05869-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="05869-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05869-107">EXAMPLES</span></span>

### <span data-ttu-id="05869-108">Esempio 1: Creazione e rimozione di un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="05869-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="05869-109">Questo esempio mostra come creare un ambiente con Add-AzEnvironment e quindi come eliminare l'ambiente con Remove-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="05869-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="05869-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05869-110">PARAMETERS</span></span>

### <span data-ttu-id="05869-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05869-111">-DefaultProfile</span></span>
<span data-ttu-id="05869-112">Le credenziali, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05869-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05869-113">-Name</span><span class="sxs-lookup"><span data-stu-id="05869-113">-Name</span></span>
<span data-ttu-id="05869-114">Specifica il nome dell'ambiente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="05869-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="05869-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="05869-115">-Scope</span></span>
<span data-ttu-id="05869-116">Determina l'ambito delle modifiche di contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="05869-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="05869-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05869-117">-Confirm</span></span>
<span data-ttu-id="05869-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05869-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05869-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05869-119">-WhatIf</span></span>
<span data-ttu-id="05869-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05869-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05869-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05869-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05869-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05869-122">CommonParameters</span></span>
<span data-ttu-id="05869-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05869-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05869-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="05869-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05869-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="05869-125">INPUTS</span></span>

### <span data-ttu-id="05869-126">System.String</span><span class="sxs-lookup"><span data-stu-id="05869-126">System.String</span></span>

## <span data-ttu-id="05869-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05869-127">OUTPUTS</span></span>

### <span data-ttu-id="05869-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="05869-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="05869-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="05869-129">NOTES</span></span>

## <span data-ttu-id="05869-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05869-130">RELATED LINKS</span></span>

[<span data-ttu-id="05869-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="05869-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="05869-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="05869-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="05869-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="05869-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

