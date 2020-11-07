---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 556b7fa95e005ff3622b64ba00d48df5e8c33339
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673741"
---
# <span data-ttu-id="a025d-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a025d-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="a025d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a025d-102">SYNOPSIS</span></span>
<span data-ttu-id="a025d-103">Rimuove gli endpoint e i metadati per la connessione a una determinata istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="a025d-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="a025d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a025d-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a025d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a025d-105">DESCRIPTION</span></span>
<span data-ttu-id="a025d-106">Il cmdlet Remove-AzEnvironment rimuove gli endpoint e le informazioni sui metadati per la connessione a una determinata istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="a025d-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="a025d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a025d-107">EXAMPLES</span></span>

### <span data-ttu-id="a025d-108">Esempio 1: creazione e rimozione di un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="a025d-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="a025d-109">Questo esempio Mostra come creare un ambiente usando Add-AzEnvironment e quindi come eliminare l'ambiente tramite Remove-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="a025d-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="a025d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a025d-110">PARAMETERS</span></span>

### <span data-ttu-id="a025d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a025d-111">-DefaultProfile</span></span>
<span data-ttu-id="a025d-112">Le credenziali, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a025d-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a025d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a025d-113">-Name</span></span>
<span data-ttu-id="a025d-114">Specifica il nome dell'ambiente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a025d-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="a025d-115">-Ambito</span><span class="sxs-lookup"><span data-stu-id="a025d-115">-Scope</span></span>
<span data-ttu-id="a025d-116">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="a025d-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a025d-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a025d-117">-Confirm</span></span>
<span data-ttu-id="a025d-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a025d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a025d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a025d-119">-WhatIf</span></span>
<span data-ttu-id="a025d-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a025d-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a025d-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a025d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a025d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a025d-122">CommonParameters</span></span>
<span data-ttu-id="a025d-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a025d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a025d-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a025d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a025d-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a025d-125">INPUTS</span></span>

### <span data-ttu-id="a025d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a025d-126">System.String</span></span>

## <span data-ttu-id="a025d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a025d-127">OUTPUTS</span></span>

### <span data-ttu-id="a025d-128">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a025d-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="a025d-129">Note</span><span class="sxs-lookup"><span data-stu-id="a025d-129">NOTES</span></span>

## <span data-ttu-id="a025d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a025d-130">RELATED LINKS</span></span>

[<span data-ttu-id="a025d-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a025d-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="a025d-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a025d-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="a025d-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a025d-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)
