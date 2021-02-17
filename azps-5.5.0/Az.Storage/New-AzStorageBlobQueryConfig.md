---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198479"
---
# <span data-ttu-id="d1cd0-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="d1cd0-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="d1cd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="d1cd0-103">Crea un oggetto di configurazione della query BLOB, che può essere usato in Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="d1cd0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1cd0-104">SYNTAX</span></span>

### <span data-ttu-id="d1cd0-105">CSV (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1cd0-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="d1cd0-106">Json</span><span class="sxs-lookup"><span data-stu-id="d1cd0-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="d1cd0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d1cd0-107">DESCRIPTION</span></span>
<span data-ttu-id="d1cd0-108">Il cmdlet **New-AzStorageBlobQueryConfig** crea un oggetto di configurazione della query BLOB, che può essere usato in Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="d1cd0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1cd0-109">EXAMPLES</span></span>

### <span data-ttu-id="d1cd0-110">Esempio 1: Creare query BLOB configura ed esegue una query su un BLOB</span><span class="sxs-lookup"><span data-stu-id="d1cd0-110">Example 1: Create blob query configures , and query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="d1cd0-111">Questo comando crea prima l'oggetto configurazione di input come CSV e l'oggetto configurazione di output come json, quindi usa le due configurazioni per eseguire query BLOB.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="d1cd0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1cd0-112">PARAMETERS</span></span>

### <span data-ttu-id="d1cd0-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="d1cd0-113">-AsCsv</span></span>
<span data-ttu-id="d1cd0-114">Indicare di creare una configurazione di query BLOB per CSV.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1cd0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1cd0-115">-AsJob</span></span>
<span data-ttu-id="d1cd0-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d1cd0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1cd0-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="d1cd0-117">-AsJson</span></span>
<span data-ttu-id="d1cd0-118">Indicare di creare una configurazione di query BLOB per Json.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-118">Indicate to create a Blob Query Configuration for Json.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Json
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1cd0-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="d1cd0-119">-ColumnSeparator</span></span>
<span data-ttu-id="d1cd0-120">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-120">Optional.</span></span>
<span data-ttu-id="d1cd0-121">Stringa usata per separare le colonne.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-121">The string used to separate columns.</span></span>

```yaml
Type: System.String
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1cd0-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="d1cd0-122">-EscapeCharacter</span></span>
<span data-ttu-id="d1cd0-123">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-123">Optional.</span></span>
<span data-ttu-id="d1cd0-124">Valore char usato come carattere di escape.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-124">The char used as an escape character.</span></span>

```yaml
Type: System.Nullable`1[System.Char]
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1cd0-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="d1cd0-125">-HasHeader</span></span>
<span data-ttu-id="d1cd0-126">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-126">Optional.</span></span>
<span data-ttu-id="d1cd0-127">Indicare che i dati hanno intestazioni.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-127">Indicate it represent the data has headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1cd0-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="d1cd0-128">-QuotationCharacter</span></span>
<span data-ttu-id="d1cd0-129">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-129">Optional.</span></span>
<span data-ttu-id="d1cd0-130">Valore char usato per citare un campo specifico.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-130">The char used to quote a specific field.</span></span>

```yaml
Type: System.Char
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1cd0-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="d1cd0-131">-RecordSeparator</span></span>
<span data-ttu-id="d1cd0-132">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-132">Optional.</span></span>
<span data-ttu-id="d1cd0-133">Stringa usata per separare i record.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="d1cd0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1cd0-134">CommonParameters</span></span>
<span data-ttu-id="d1cd0-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1cd0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1cd0-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1cd0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1cd0-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="d1cd0-137">INPUTS</span></span>

### <span data-ttu-id="d1cd0-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d1cd0-138">None</span></span>

## <span data-ttu-id="d1cd0-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1cd0-139">OUTPUTS</span></span>

### <span data-ttu-id="d1cd0-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1cd0-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="d1cd0-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="d1cd0-141">NOTES</span></span>

## <span data-ttu-id="d1cd0-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1cd0-142">RELATED LINKS</span></span>
