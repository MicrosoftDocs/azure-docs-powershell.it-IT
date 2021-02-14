---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190007"
---
# <span data-ttu-id="f1124-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f1124-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="f1124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1124-102">SYNOPSIS</span></span>
<span data-ttu-id="f1124-103">Aggiorna un account File Azure NetApp (ANF) con il nuovo set di dati.</span><span class="sxs-lookup"><span data-stu-id="f1124-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="f1124-104">Utile per l'eliminazione di directory attive associate.</span><span class="sxs-lookup"><span data-stu-id="f1124-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="f1124-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1124-105">SYNTAX</span></span>

### <span data-ttu-id="f1124-106">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f1124-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1124-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="f1124-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1124-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f1124-108">DESCRIPTION</span></span>
<span data-ttu-id="f1124-109">Il cmdlet **Set-AzNetAppFilesAccount** modifica un account ANF.</span><span class="sxs-lookup"><span data-stu-id="f1124-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="f1124-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1124-110">EXAMPLES</span></span>

### <span data-ttu-id="f1124-111">Esempio 1: Modificare un account ANF</span><span class="sxs-lookup"><span data-stu-id="f1124-111">Example 1 : Modify an ANF account</span></span>
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

<span data-ttu-id="f1124-112">Questo comando esegue un aggiornamento per l'account specificato.</span><span class="sxs-lookup"><span data-stu-id="f1124-112">This command performs an update on the given account.</span></span> <span data-ttu-id="f1124-113">L'assenza di Active Directory significa che verrà rimossa dall'account.</span><span class="sxs-lookup"><span data-stu-id="f1124-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="f1124-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1124-114">PARAMETERS</span></span>

### <span data-ttu-id="f1124-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="f1124-115">-ActiveDirectory</span></span>
<span data-ttu-id="f1124-116">Matrice di tabella hash che rappresenta le directory attive</span><span class="sxs-lookup"><span data-stu-id="f1124-116">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="f1124-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1124-117">-DefaultProfile</span></span>
<span data-ttu-id="f1124-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1124-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1124-119">-Location</span><span class="sxs-lookup"><span data-stu-id="f1124-119">-Location</span></span>
<span data-ttu-id="f1124-120">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="f1124-120">The location of the resource</span></span>

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

### <span data-ttu-id="f1124-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f1124-121">-Name</span></span>
<span data-ttu-id="f1124-122">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="f1124-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="f1124-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1124-123">-ResourceGroupName</span></span>
<span data-ttu-id="f1124-124">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="f1124-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f1124-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="f1124-125">-Tag</span></span>
<span data-ttu-id="f1124-126">Tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="f1124-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="f1124-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1124-127">-Confirm</span></span>
<span data-ttu-id="f1124-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1124-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1124-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1124-129">-WhatIf</span></span>
<span data-ttu-id="f1124-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1124-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1124-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1124-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1124-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1124-132">CommonParameters</span></span>
<span data-ttu-id="f1124-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1124-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1124-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f1124-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1124-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="f1124-135">INPUTS</span></span>

### <span data-ttu-id="f1124-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f1124-136">None</span></span>

## <span data-ttu-id="f1124-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1124-137">OUTPUTS</span></span>

### <span data-ttu-id="f1124-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f1124-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="f1124-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="f1124-139">NOTES</span></span>

## <span data-ttu-id="f1124-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1124-140">RELATED LINKS</span></span>
