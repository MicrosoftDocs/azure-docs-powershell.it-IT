---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200640"
---
# <span data-ttu-id="7bc3e-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="7bc3e-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="7bc3e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7bc3e-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc3e-103">Crea un oggetto di configurazione della query BLOB, che può essere usato in Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="7bc3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bc3e-104">SYNTAX</span></span>

### <span data-ttu-id="7bc3e-105">CSV (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7bc3e-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="7bc3e-106">JSON</span><span class="sxs-lookup"><span data-stu-id="7bc3e-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="7bc3e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bc3e-107">DESCRIPTION</span></span>
<span data-ttu-id="7bc3e-108">Il cmdlet **New-AzStorageBlobQueryConfig** crea un oggetto di configurazione della query BLOB, che può essere usato in Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="7bc3e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bc3e-109">EXAMPLES</span></span>

### <span data-ttu-id="7bc3e-110">Esempio 1: creare una query BLOB configura e eseguire una query su un BLOB</span><span class="sxs-lookup"><span data-stu-id="7bc3e-110">Example 1: Create blob query configures , and query a blob</span></span>
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

<span data-ttu-id="7bc3e-111">Questo comando crea prima di tutto l'oggetto configurazione di input come CSV e l'oggetto di configurazione di output come JSON, quindi usa le 2 configurazioni per eseguire query su BLOB.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="7bc3e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7bc3e-112">PARAMETERS</span></span>

### <span data-ttu-id="7bc3e-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="7bc3e-113">-AsCsv</span></span>
<span data-ttu-id="7bc3e-114">Indicare la creazione di una configurazione di query BLOB per CSV.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

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

### <span data-ttu-id="7bc3e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bc3e-115">-AsJob</span></span>
<span data-ttu-id="7bc3e-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7bc3e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7bc3e-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="7bc3e-117">-AsJson</span></span>
<span data-ttu-id="7bc3e-118">Indicare la creazione di una configurazione di query BLOB per JSON.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-118">Indicate to create a Blob Query Configuration for Json.</span></span>

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

### <span data-ttu-id="7bc3e-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="7bc3e-119">-ColumnSeparator</span></span>
<span data-ttu-id="7bc3e-120">Opzionale.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-120">Optional.</span></span>
<span data-ttu-id="7bc3e-121">Stringa usata per separare le colonne.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-121">The string used to separate columns.</span></span>

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

### <span data-ttu-id="7bc3e-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="7bc3e-122">-EscapeCharacter</span></span>
<span data-ttu-id="7bc3e-123">Opzionale.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-123">Optional.</span></span>
<span data-ttu-id="7bc3e-124">Char usato come carattere di escape.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-124">The char used as an escape character.</span></span>

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

### <span data-ttu-id="7bc3e-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="7bc3e-125">-HasHeader</span></span>
<span data-ttu-id="7bc3e-126">Opzionale.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-126">Optional.</span></span>
<span data-ttu-id="7bc3e-127">Indica che rappresentano i dati con intestazioni.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-127">Indicate it represent the data has headers.</span></span>

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

### <span data-ttu-id="7bc3e-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="7bc3e-128">-QuotationCharacter</span></span>
<span data-ttu-id="7bc3e-129">Opzionale.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-129">Optional.</span></span>
<span data-ttu-id="7bc3e-130">Il carattere usato per citare un campo specifico.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-130">The char used to quote a specific field.</span></span>

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

### <span data-ttu-id="7bc3e-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="7bc3e-131">-RecordSeparator</span></span>
<span data-ttu-id="7bc3e-132">Opzionale.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-132">Optional.</span></span>
<span data-ttu-id="7bc3e-133">Stringa usata per separare i record.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="7bc3e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc3e-134">CommonParameters</span></span>
<span data-ttu-id="7bc3e-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc3e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc3e-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc3e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc3e-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7bc3e-137">INPUTS</span></span>

### <span data-ttu-id="7bc3e-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7bc3e-138">None</span></span>

## <span data-ttu-id="7bc3e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bc3e-139">OUTPUTS</span></span>

### <span data-ttu-id="7bc3e-140">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bc3e-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="7bc3e-141">Note</span><span class="sxs-lookup"><span data-stu-id="7bc3e-141">NOTES</span></span>

## <span data-ttu-id="7bc3e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bc3e-142">RELATED LINKS</span></span>
