---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 7294d5c48bd8cbc94ac127ac1f1543827dc2937b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995607"
---
# <span data-ttu-id="d19db-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d19db-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="d19db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d19db-102">SYNOPSIS</span></span>
<span data-ttu-id="d19db-103">Modifica l'ottale di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d19db-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d19db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d19db-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d19db-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d19db-105">DESCRIPTION</span></span>
<span data-ttu-id="d19db-106">Il cmdlet **Set-AzDataLakeStoreItemPermission** modifica l'ottale di autorizzazione di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d19db-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d19db-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d19db-107">EXAMPLES</span></span>

### <span data-ttu-id="d19db-108">Esempio 1: Impostare l'ottale di autorizzazione per un elemento</span><span class="sxs-lookup"><span data-stu-id="d19db-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="d19db-109">Questo comando imposta l'ottale di autorizzazione per un file su 0770, ovvero cancella il bit del messaggio, imposta le autorizzazioni di lettura/scrittura/esecuzione per il proprietario del file, imposta le autorizzazioni di lettura/scrittura/esecuzione per il gruppo proprietario del file e deseleziona le autorizzazioni di lettura/scrittura/esecuzione per altri utenti.</span><span class="sxs-lookup"><span data-stu-id="d19db-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="d19db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d19db-110">PARAMETERS</span></span>

### <span data-ttu-id="d19db-111">-Account</span><span class="sxs-lookup"><span data-stu-id="d19db-111">-Account</span></span>
<span data-ttu-id="d19db-112">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d19db-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="d19db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d19db-113">-DefaultProfile</span></span>
<span data-ttu-id="d19db-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d19db-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d19db-115">-Path</span><span class="sxs-lookup"><span data-stu-id="d19db-115">-Path</span></span>
<span data-ttu-id="d19db-116">Specifica il percorso Data Lake Store del file o della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="d19db-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d19db-117">-Permission</span><span class="sxs-lookup"><span data-stu-id="d19db-117">-Permission</span></span>
<span data-ttu-id="d19db-118">Autorizzazioni da impostare per il file o la cartella, espresse come ottale (ad esempio "777")</span><span class="sxs-lookup"><span data-stu-id="d19db-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d19db-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d19db-119">-Confirm</span></span>
<span data-ttu-id="d19db-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d19db-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d19db-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d19db-121">-WhatIf</span></span>
<span data-ttu-id="d19db-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d19db-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d19db-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d19db-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d19db-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d19db-124">CommonParameters</span></span>
<span data-ttu-id="d19db-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d19db-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d19db-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d19db-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d19db-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="d19db-127">INPUTS</span></span>

### <span data-ttu-id="d19db-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d19db-128">System.String</span></span>

### <span data-ttu-id="d19db-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d19db-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d19db-130">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d19db-130">System.Int32</span></span>

## <span data-ttu-id="d19db-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d19db-131">OUTPUTS</span></span>

### <span data-ttu-id="d19db-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d19db-132">System.Boolean</span></span>

## <span data-ttu-id="d19db-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="d19db-133">NOTES</span></span>
* <span data-ttu-id="d19db-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d19db-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="d19db-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d19db-135">RELATED LINKS</span></span>

[<span data-ttu-id="d19db-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d19db-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


