---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: c5b8059561b859bd4ea7698b2cb41c9eb9a50a51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968221"
---
# <span data-ttu-id="a96f0-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a96f0-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="a96f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a96f0-102">SYNOPSIS</span></span>
<span data-ttu-id="a96f0-103">Aggiorna un account File Azure NetApp (ANF) con il nuovo set di dati.</span><span class="sxs-lookup"><span data-stu-id="a96f0-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="a96f0-104">Utile per l'eliminazione di directory attive associate.</span><span class="sxs-lookup"><span data-stu-id="a96f0-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="a96f0-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a96f0-105">SYNTAX</span></span>

### <span data-ttu-id="a96f0-106">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a96f0-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a96f0-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a96f0-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a96f0-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a96f0-108">DESCRIPTION</span></span>
<span data-ttu-id="a96f0-109">Il cmdlet **Set-AzNetAppFilesAccount** modifica un account ANF.</span><span class="sxs-lookup"><span data-stu-id="a96f0-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="a96f0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a96f0-110">EXAMPLES</span></span>

### <span data-ttu-id="a96f0-111">Esempio 1: Modificare un account ANF</span><span class="sxs-lookup"><span data-stu-id="a96f0-111">Example 1 : Modify an ANF account</span></span>
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

<span data-ttu-id="a96f0-112">Questo comando esegue un aggiornamento per l'account specificato.</span><span class="sxs-lookup"><span data-stu-id="a96f0-112">This command performs an update on the given account.</span></span> <span data-ttu-id="a96f0-113">L'assenza di Active Directory significa che verrà rimossa dall'account.</span><span class="sxs-lookup"><span data-stu-id="a96f0-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="a96f0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a96f0-114">PARAMETERS</span></span>

### <span data-ttu-id="a96f0-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a96f0-115">-ActiveDirectory</span></span>
<span data-ttu-id="a96f0-116">Matrice di tabella hash che rappresenta le directory attive</span><span class="sxs-lookup"><span data-stu-id="a96f0-116">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="a96f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a96f0-117">-DefaultProfile</span></span>
<span data-ttu-id="a96f0-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a96f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a96f0-119">-Location</span><span class="sxs-lookup"><span data-stu-id="a96f0-119">-Location</span></span>
<span data-ttu-id="a96f0-120">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="a96f0-120">The location of the resource</span></span>

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

### <span data-ttu-id="a96f0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a96f0-121">-Name</span></span>
<span data-ttu-id="a96f0-122">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="a96f0-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="a96f0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a96f0-123">-ResourceGroupName</span></span>
<span data-ttu-id="a96f0-124">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="a96f0-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a96f0-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="a96f0-125">-Tag</span></span>
<span data-ttu-id="a96f0-126">Tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="a96f0-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="a96f0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a96f0-127">-Confirm</span></span>
<span data-ttu-id="a96f0-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a96f0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a96f0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a96f0-129">-WhatIf</span></span>
<span data-ttu-id="a96f0-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a96f0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a96f0-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a96f0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a96f0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a96f0-132">CommonParameters</span></span>
<span data-ttu-id="a96f0-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a96f0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a96f0-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a96f0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a96f0-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="a96f0-135">INPUTS</span></span>

### <span data-ttu-id="a96f0-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a96f0-136">None</span></span>

## <span data-ttu-id="a96f0-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a96f0-137">OUTPUTS</span></span>

### <span data-ttu-id="a96f0-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a96f0-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="a96f0-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="a96f0-139">NOTES</span></span>

## <span data-ttu-id="a96f0-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a96f0-140">RELATED LINKS</span></span>
