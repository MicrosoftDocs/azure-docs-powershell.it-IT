---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 48edcb93cb8fce66c9175bdcf498bd6545949090
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519196"
---
# <span data-ttu-id="521c2-101">Remove-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="521c2-101">Remove-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="521c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="521c2-102">SYNOPSIS</span></span>
<span data-ttu-id="521c2-103">Cancella l'ACL di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="521c2-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="521c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="521c2-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="521c2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="521c2-105">DESCRIPTION</span></span>
<span data-ttu-id="521c2-106">Il cmdlet **Remove-AzureRmDataLakeStoreItemAcl** cancella l'elenco di controllo di accesso (ACL) di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="521c2-106">The **Remove-AzureRmDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="521c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="521c2-107">EXAMPLES</span></span>

### <span data-ttu-id="521c2-108">Esempio 1: rimuovere l'ACL da una cartella</span><span class="sxs-lookup"><span data-stu-id="521c2-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="521c2-109">Questo comando rimuove l'ACL per la directory radice per l'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="521c2-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="521c2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="521c2-110">PARAMETERS</span></span>

### <span data-ttu-id="521c2-111">-Account</span><span class="sxs-lookup"><span data-stu-id="521c2-111">-Account</span></span>
<span data-ttu-id="521c2-112">Specifica il nome dell'account Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="521c2-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="521c2-113">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="521c2-113">-Default</span></span>
<span data-ttu-id="521c2-114">Indica che il cmdlet rimuove l'ACL predefinito per un file o una cartella.</span><span class="sxs-lookup"><span data-stu-id="521c2-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="521c2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="521c2-115">-Force</span></span>
<span data-ttu-id="521c2-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="521c2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="521c2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="521c2-117">-PassThru</span></span>
<span data-ttu-id="521c2-118">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="521c2-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="521c2-119">-Path</span><span class="sxs-lookup"><span data-stu-id="521c2-119">-Path</span></span>
<span data-ttu-id="521c2-120">Specifica il percorso dello Store Data Lake dell'elemento, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="521c2-120">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="521c2-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="521c2-121">-Confirm</span></span>
<span data-ttu-id="521c2-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="521c2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="521c2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="521c2-123">-WhatIf</span></span>
<span data-ttu-id="521c2-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="521c2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="521c2-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="521c2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="521c2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521c2-126">-DefaultProfile</span></span>
<span data-ttu-id="521c2-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="521c2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521c2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521c2-128">CommonParameters</span></span>
<span data-ttu-id="521c2-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="521c2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521c2-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="521c2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521c2-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="521c2-131">INPUTS</span></span>

## <span data-ttu-id="521c2-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="521c2-132">OUTPUTS</span></span>

### <span data-ttu-id="521c2-133">bool</span><span class="sxs-lookup"><span data-stu-id="521c2-133">bool</span></span>
<span data-ttu-id="521c2-134">Se PassThru è specificato, restituisce vero al completamento corretto.</span><span class="sxs-lookup"><span data-stu-id="521c2-134">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="521c2-135">Note</span><span class="sxs-lookup"><span data-stu-id="521c2-135">NOTES</span></span>
* <span data-ttu-id="521c2-136">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="521c2-136">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="521c2-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="521c2-137">RELATED LINKS</span></span>

[<span data-ttu-id="521c2-138">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="521c2-138">Get-AzureRmDataLakeStoreItemAclEntry</span></span>](./Get-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="521c2-139">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="521c2-139">Set-AzureRmDataLakeStoreItemAcl</span></span>](./Set-AzureRmDataLakeStoreItemAcl.md)

[<span data-ttu-id="521c2-140">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="521c2-140">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


