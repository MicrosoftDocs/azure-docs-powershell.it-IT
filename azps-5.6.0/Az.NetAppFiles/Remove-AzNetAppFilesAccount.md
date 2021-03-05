---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 19f194d9402c2d5101b1da56c7c7a2a2208345aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968382"
---
# <span data-ttu-id="75114-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="75114-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="75114-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75114-102">SYNOPSIS</span></span>
<span data-ttu-id="75114-103">Elimina un account FILE (ANF) di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="75114-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="75114-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75114-104">SYNTAX</span></span>

### <span data-ttu-id="75114-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75114-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75114-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75114-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75114-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75114-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75114-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="75114-108">DESCRIPTION</span></span>
<span data-ttu-id="75114-109">Il cmdlet **Remove-AzNetAppFilesAccount** elimina un account ANF.</span><span class="sxs-lookup"><span data-stu-id="75114-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="75114-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75114-110">EXAMPLES</span></span>

### <span data-ttu-id="75114-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75114-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="75114-112">Questo comando elimina l'account ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="75114-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="75114-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75114-113">PARAMETERS</span></span>

### <span data-ttu-id="75114-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75114-114">-DefaultProfile</span></span>
<span data-ttu-id="75114-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75114-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75114-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75114-116">-InputObject</span></span>
<span data-ttu-id="75114-117">Oggetto account da rimuovere</span><span class="sxs-lookup"><span data-stu-id="75114-117">The account object to remove</span></span>

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

### <span data-ttu-id="75114-118">-Name</span><span class="sxs-lookup"><span data-stu-id="75114-118">-Name</span></span>
<span data-ttu-id="75114-119">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="75114-119">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75114-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75114-120">-PassThru</span></span>
<span data-ttu-id="75114-121">Restituire se l'account specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="75114-121">Return whether the specified account was successfully removed</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75114-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75114-122">-ResourceGroupName</span></span>
<span data-ttu-id="75114-123">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="75114-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="75114-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75114-124">-ResourceId</span></span>
<span data-ttu-id="75114-125">ID risorsa dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="75114-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="75114-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75114-126">-Confirm</span></span>
<span data-ttu-id="75114-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75114-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75114-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75114-128">-WhatIf</span></span>
<span data-ttu-id="75114-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75114-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75114-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75114-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75114-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75114-131">CommonParameters</span></span>
<span data-ttu-id="75114-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75114-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75114-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75114-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75114-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="75114-134">INPUTS</span></span>

### <span data-ttu-id="75114-135">System.String</span><span class="sxs-lookup"><span data-stu-id="75114-135">System.String</span></span>

### <span data-ttu-id="75114-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="75114-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="75114-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75114-137">OUTPUTS</span></span>

### <span data-ttu-id="75114-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="75114-138">System.Boolean</span></span>

## <span data-ttu-id="75114-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="75114-139">NOTES</span></span>

## <span data-ttu-id="75114-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75114-140">RELATED LINKS</span></span>
