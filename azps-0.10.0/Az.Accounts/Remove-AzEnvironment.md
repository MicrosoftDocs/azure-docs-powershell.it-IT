---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: fa16d5f534a0bb26c0976cbc75700f7390f62466
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860190"
---
# <span data-ttu-id="2c7e6-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="2c7e6-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="2c7e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c7e6-102">SYNOPSIS</span></span>
<span data-ttu-id="2c7e6-103">Rimuove gli endpoint e i metadati per la connessione a una determinata istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7e6-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="2c7e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c7e6-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c7e6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c7e6-105">DESCRIPTION</span></span>
<span data-ttu-id="2c7e6-106">Il cmdlet Remove-AzEnvironment rimuove gli endpoint e le informazioni sui metadati per la connessione a una determinata istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7e6-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="2c7e6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c7e6-107">EXAMPLES</span></span>

### <span data-ttu-id="2c7e6-108">Esempio 1: creazione e rimozione di un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="2c7e6-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="2c7e6-109">Questo esempio Mostra come creare un ambiente usando Add-AzEnvironment e quindi come eliminare l'ambiente tramite Remove-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="2c7e6-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="2c7e6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c7e6-110">PARAMETERS</span></span>

### <span data-ttu-id="2c7e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c7e6-111">-DefaultProfile</span></span>
<span data-ttu-id="2c7e6-112">Le credenziali, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7e6-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c7e6-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c7e6-113">-Name</span></span>
<span data-ttu-id="2c7e6-114">Specifica il nome dell'ambiente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2c7e6-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="2c7e6-115">-Ambito</span><span class="sxs-lookup"><span data-stu-id="2c7e6-115">-Scope</span></span>
<span data-ttu-id="2c7e6-116">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="2c7e6-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="2c7e6-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2c7e6-117">-Confirm</span></span>
<span data-ttu-id="2c7e6-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c7e6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c7e6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c7e6-119">-WhatIf</span></span>
<span data-ttu-id="2c7e6-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c7e6-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c7e6-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c7e6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c7e6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c7e6-122">CommonParameters</span></span>
<span data-ttu-id="2c7e6-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c7e6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c7e6-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c7e6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c7e6-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c7e6-125">INPUTS</span></span>

### <span data-ttu-id="2c7e6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2c7e6-126">System.String</span></span>

## <span data-ttu-id="2c7e6-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c7e6-127">OUTPUTS</span></span>

### <span data-ttu-id="2c7e6-128">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="2c7e6-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="2c7e6-129">Note</span><span class="sxs-lookup"><span data-stu-id="2c7e6-129">NOTES</span></span>

## <span data-ttu-id="2c7e6-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c7e6-130">RELATED LINKS</span></span>

[<span data-ttu-id="2c7e6-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="2c7e6-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="2c7e6-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="2c7e6-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="2c7e6-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="2c7e6-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

