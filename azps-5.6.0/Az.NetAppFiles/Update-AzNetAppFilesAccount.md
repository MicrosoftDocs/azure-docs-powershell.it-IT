---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 2a31b5af374b1bc0f6136da61aa1c3672274e913
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968142"
---
# <span data-ttu-id="51158-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="51158-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="51158-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51158-102">SYNOPSIS</span></span>
<span data-ttu-id="51158-103">Aggiorna un account Dei file ANF (Azure NetApp Files) in base ai modificatori facoltativi disponibili.</span><span class="sxs-lookup"><span data-stu-id="51158-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="51158-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51158-104">SYNTAX</span></span>

### <span data-ttu-id="51158-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="51158-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51158-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51158-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51158-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51158-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51158-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="51158-108">DESCRIPTION</span></span>
<span data-ttu-id="51158-109">Il cmdlet **Update-AzNetAppFilesAccount** modifica un account ANF.</span><span class="sxs-lookup"><span data-stu-id="51158-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="51158-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51158-110">EXAMPLES</span></span>

### <span data-ttu-id="51158-111">Esempio 1: Aggiorna un account ANF</span><span class="sxs-lookup"><span data-stu-id="51158-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="51158-112">Questo comando esegue un aggiornamento sull'account specificato modificando i tag in base a quelli forniti.</span><span class="sxs-lookup"><span data-stu-id="51158-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="51158-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51158-113">PARAMETERS</span></span>

### <span data-ttu-id="51158-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="51158-114">-ActiveDirectory</span></span>
<span data-ttu-id="51158-115">Matrice di tabella hash che rappresenta le directory attive</span><span class="sxs-lookup"><span data-stu-id="51158-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51158-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51158-116">-DefaultProfile</span></span>
<span data-ttu-id="51158-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51158-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51158-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51158-118">-InputObject</span></span>
<span data-ttu-id="51158-119">Oggetto account da aggiornare</span><span class="sxs-lookup"><span data-stu-id="51158-119">The account object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51158-120">-Location</span><span class="sxs-lookup"><span data-stu-id="51158-120">-Location</span></span>
<span data-ttu-id="51158-121">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="51158-121">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51158-122">-Name</span><span class="sxs-lookup"><span data-stu-id="51158-122">-Name</span></span>
<span data-ttu-id="51158-123">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="51158-123">The name of the ANF account</span></span>

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

### <span data-ttu-id="51158-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51158-124">-ResourceGroupName</span></span>
<span data-ttu-id="51158-125">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="51158-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="51158-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51158-126">-ResourceId</span></span>
<span data-ttu-id="51158-127">ID risorsa dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="51158-127">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51158-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="51158-128">-Tag</span></span>
<span data-ttu-id="51158-129">Tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="51158-129">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="51158-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51158-130">-Confirm</span></span>
<span data-ttu-id="51158-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51158-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51158-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51158-132">-WhatIf</span></span>
<span data-ttu-id="51158-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51158-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51158-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51158-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51158-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51158-135">CommonParameters</span></span>
<span data-ttu-id="51158-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51158-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51158-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="51158-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51158-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="51158-138">INPUTS</span></span>

### <span data-ttu-id="51158-139">System.String</span><span class="sxs-lookup"><span data-stu-id="51158-139">System.String</span></span>

### <span data-ttu-id="51158-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="51158-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="51158-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51158-141">OUTPUTS</span></span>

### <span data-ttu-id="51158-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="51158-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="51158-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="51158-143">NOTES</span></span>

## <span data-ttu-id="51158-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51158-144">RELATED LINKS</span></span>
