---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 9b762a2fe0f12483fd664b8862e483b1b948bc75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971133"
---
# <span data-ttu-id="fc177-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="fc177-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="fc177-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc177-102">SYNOPSIS</span></span>
<span data-ttu-id="fc177-103">Cancella l'ACL di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fc177-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fc177-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc177-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc177-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fc177-105">DESCRIPTION</span></span>
<span data-ttu-id="fc177-106">Il cmdlet **Remove-AzDataLakeStoreItemAcl** cancella l'elenco di controllo di accesso (ACL) di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fc177-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fc177-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc177-107">EXAMPLES</span></span>

### <span data-ttu-id="fc177-108">Esempio 1: Rimuovere l'ACL da una cartella</span><span class="sxs-lookup"><span data-stu-id="fc177-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="fc177-109">Questo comando rimuove l'ACL per la directory radice dell'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="fc177-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="fc177-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc177-110">PARAMETERS</span></span>

### <span data-ttu-id="fc177-111">-Account</span><span class="sxs-lookup"><span data-stu-id="fc177-111">-Account</span></span>
<span data-ttu-id="fc177-112">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fc177-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc177-113">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="fc177-113">-Default</span></span>
<span data-ttu-id="fc177-114">Indica che il cmdlet rimuove l'ACL predefinito per un file o una cartella.</span><span class="sxs-lookup"><span data-stu-id="fc177-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc177-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc177-115">-DefaultProfile</span></span>
<span data-ttu-id="fc177-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc177-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc177-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fc177-117">-Force</span></span>
<span data-ttu-id="fc177-118">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="fc177-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc177-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc177-119">-PassThru</span></span>
<span data-ttu-id="fc177-120">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="fc177-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc177-121">-Path</span><span class="sxs-lookup"><span data-stu-id="fc177-121">-Path</span></span>
<span data-ttu-id="fc177-122">Specifica il percorso Data Lake Store dell'elemento, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="fc177-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc177-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc177-123">-Confirm</span></span>
<span data-ttu-id="fc177-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc177-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc177-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc177-125">-WhatIf</span></span>
<span data-ttu-id="fc177-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc177-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc177-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc177-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc177-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc177-128">CommonParameters</span></span>
<span data-ttu-id="fc177-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc177-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc177-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc177-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc177-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="fc177-131">INPUTS</span></span>

### <span data-ttu-id="fc177-132">System.String</span><span class="sxs-lookup"><span data-stu-id="fc177-132">System.String</span></span>

### <span data-ttu-id="fc177-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="fc177-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="fc177-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fc177-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fc177-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc177-135">OUTPUTS</span></span>

### <span data-ttu-id="fc177-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fc177-136">System.Boolean</span></span>

## <span data-ttu-id="fc177-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="fc177-137">NOTES</span></span>
* <span data-ttu-id="fc177-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="fc177-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="fc177-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc177-139">RELATED LINKS</span></span>

[<span data-ttu-id="fc177-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fc177-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="fc177-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="fc177-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="fc177-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fc177-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


