---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380516"
---
# <span data-ttu-id="06d32-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="06d32-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="06d32-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06d32-102">SYNOPSIS</span></span>
<span data-ttu-id="06d32-103">Aggiorna un account di Azure NetApp file (ANF) con il nuovo set di dati.</span><span class="sxs-lookup"><span data-stu-id="06d32-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="06d32-104">Utile per l'eliminazione di Active Directory associate.</span><span class="sxs-lookup"><span data-stu-id="06d32-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="06d32-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06d32-105">SYNTAX</span></span>

### <span data-ttu-id="06d32-106">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="06d32-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06d32-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="06d32-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06d32-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06d32-108">DESCRIPTION</span></span>
<span data-ttu-id="06d32-109">Il cmdlet **set-AzNetAppFilesAccount** modifica un account ANF.</span><span class="sxs-lookup"><span data-stu-id="06d32-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="06d32-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06d32-110">EXAMPLES</span></span>

### <span data-ttu-id="06d32-111">Esempio 1: modificare un account di ANF</span><span class="sxs-lookup"><span data-stu-id="06d32-111">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="06d32-112">Questo comando esegue un aggiornamento per l'account specifico.</span><span class="sxs-lookup"><span data-stu-id="06d32-112">This command performs an update on the given account.</span></span> <span data-ttu-id="06d32-113">L'assenza di Active Directory significa che verrà rimossa dall'account.</span><span class="sxs-lookup"><span data-stu-id="06d32-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="06d32-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06d32-114">PARAMETERS</span></span>

### <span data-ttu-id="06d32-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="06d32-115">-ActiveDirectory</span></span>
<span data-ttu-id="06d32-116">Matrice Hashtable che rappresenta le directory attive</span><span class="sxs-lookup"><span data-stu-id="06d32-116">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: SetByResourceActiveDirectory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d32-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d32-117">-DefaultProfile</span></span>
<span data-ttu-id="06d32-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06d32-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06d32-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="06d32-119">-Location</span></span>
<span data-ttu-id="06d32-120">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="06d32-120">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d32-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="06d32-121">-Name</span></span>
<span data-ttu-id="06d32-122">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="06d32-122">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d32-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d32-123">-ResourceGroupName</span></span>
<span data-ttu-id="06d32-124">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="06d32-124">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d32-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="06d32-125">-Tag</span></span>
<span data-ttu-id="06d32-126">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="06d32-126">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d32-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06d32-127">-Confirm</span></span>
<span data-ttu-id="06d32-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06d32-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d32-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06d32-129">-WhatIf</span></span>
<span data-ttu-id="06d32-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06d32-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06d32-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06d32-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d32-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d32-132">CommonParameters</span></span>
<span data-ttu-id="06d32-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d32-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d32-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06d32-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d32-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06d32-135">INPUTS</span></span>

### <span data-ttu-id="06d32-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="06d32-136">None</span></span>

## <span data-ttu-id="06d32-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06d32-137">OUTPUTS</span></span>

### <span data-ttu-id="06d32-138">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="06d32-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="06d32-139">Note</span><span class="sxs-lookup"><span data-stu-id="06d32-139">NOTES</span></span>

## <span data-ttu-id="06d32-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06d32-140">RELATED LINKS</span></span>
