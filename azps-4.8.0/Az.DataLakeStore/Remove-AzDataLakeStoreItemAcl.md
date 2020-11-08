---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: ed7b1a0c0c969f2593d045549f897a172a88f6aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190778"
---
# <span data-ttu-id="fa850-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="fa850-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="fa850-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa850-102">SYNOPSIS</span></span>
<span data-ttu-id="fa850-103">Cancella l'ACL di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fa850-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fa850-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa850-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa850-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa850-105">DESCRIPTION</span></span>
<span data-ttu-id="fa850-106">Il cmdlet **Remove-AzDataLakeStoreItemAcl** cancella l'elenco di controllo di accesso (ACL) di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fa850-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fa850-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa850-107">EXAMPLES</span></span>

### <span data-ttu-id="fa850-108">Esempio 1: rimuovere l'ACL da una cartella</span><span class="sxs-lookup"><span data-stu-id="fa850-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="fa850-109">Questo comando rimuove l'ACL per la directory radice per l'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="fa850-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="fa850-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa850-110">PARAMETERS</span></span>

### <span data-ttu-id="fa850-111">-Account</span><span class="sxs-lookup"><span data-stu-id="fa850-111">-Account</span></span>
<span data-ttu-id="fa850-112">Specifica il nome dell'account Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="fa850-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="fa850-113">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="fa850-113">-Default</span></span>
<span data-ttu-id="fa850-114">Indica che il cmdlet rimuove l'ACL predefinito per un file o una cartella.</span><span class="sxs-lookup"><span data-stu-id="fa850-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="fa850-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa850-115">-DefaultProfile</span></span>
<span data-ttu-id="fa850-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa850-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa850-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fa850-117">-Force</span></span>
<span data-ttu-id="fa850-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fa850-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fa850-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa850-119">-PassThru</span></span>
<span data-ttu-id="fa850-120">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="fa850-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="fa850-121">-Path</span><span class="sxs-lookup"><span data-stu-id="fa850-121">-Path</span></span>
<span data-ttu-id="fa850-122">Specifica il percorso dello Store Data Lake dell'elemento, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="fa850-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="fa850-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fa850-123">-Confirm</span></span>
<span data-ttu-id="fa850-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa850-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa850-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa850-125">-WhatIf</span></span>
<span data-ttu-id="fa850-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa850-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa850-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa850-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa850-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa850-128">CommonParameters</span></span>
<span data-ttu-id="fa850-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa850-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa850-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa850-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa850-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa850-131">INPUTS</span></span>

### <span data-ttu-id="fa850-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fa850-132">System.String</span></span>

### <span data-ttu-id="fa850-133">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="fa850-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="fa850-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fa850-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fa850-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa850-135">OUTPUTS</span></span>

### <span data-ttu-id="fa850-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa850-136">System.Boolean</span></span>

## <span data-ttu-id="fa850-137">Note</span><span class="sxs-lookup"><span data-stu-id="fa850-137">NOTES</span></span>
* <span data-ttu-id="fa850-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="fa850-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="fa850-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa850-139">RELATED LINKS</span></span>

[<span data-ttu-id="fa850-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fa850-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="fa850-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="fa850-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="fa850-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fa850-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


