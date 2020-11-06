---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517280"
---
# <span data-ttu-id="f4a73-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="f4a73-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="f4a73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4a73-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a73-103">Controlla i potenziali problemi di compatibilità tra il sistema e la sincronizzazione di file Azure.</span><span class="sxs-lookup"><span data-stu-id="f4a73-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4a73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4a73-104">SYNTAX</span></span>

### <span data-ttu-id="f4a73-105">PathBased (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4a73-105">PathBased (Default)</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### <span data-ttu-id="f4a73-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="f4a73-106">ComputerNameBased</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## <span data-ttu-id="f4a73-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4a73-107">DESCRIPTION</span></span>
<span data-ttu-id="f4a73-108">Il cmdlet **Invoke-AzureRmStorageSyncCompatibilityCheck** controlla i potenziali problemi di compatibilità tra il sistema e la sincronizzazione di file di Azure. Assegnato un percorso locale o remoto, esegue un set di convalide nello spazio dei nomi System e file e quindi restituisce i problemi di compatibilità che trova.</span><span class="sxs-lookup"><span data-stu-id="f4a73-108">The **Invoke-AzureRmStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="f4a73-109">Controlli di sistema:</span><span class="sxs-lookup"><span data-stu-id="f4a73-109">System checks:</span></span>
- <span data-ttu-id="f4a73-110">Controlli dello spazio dei nomi del file di compatibilità OS:</span><span class="sxs-lookup"><span data-stu-id="f4a73-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="f4a73-111">Caratteri non supportati</span><span class="sxs-lookup"><span data-stu-id="f4a73-111">Unsupported characters</span></span>
- <span data-ttu-id="f4a73-112">Dimensione massima del file</span><span class="sxs-lookup"><span data-stu-id="f4a73-112">Maximum file size</span></span>
- <span data-ttu-id="f4a73-113">Lunghezza massima del percorso</span><span class="sxs-lookup"><span data-stu-id="f4a73-113">Maximum path length</span></span>
- <span data-ttu-id="f4a73-114">Lunghezza massima del file</span><span class="sxs-lookup"><span data-stu-id="f4a73-114">Maximum file length</span></span>
- <span data-ttu-id="f4a73-115">Dimensioni massime del set di dati</span><span class="sxs-lookup"><span data-stu-id="f4a73-115">Maximum dataset size</span></span>
- <span data-ttu-id="f4a73-116">Profondità massima della directory</span><span class="sxs-lookup"><span data-stu-id="f4a73-116">Maximum directory depth</span></span>

## <span data-ttu-id="f4a73-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4a73-117">EXAMPLES</span></span>

### <span data-ttu-id="f4a73-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f4a73-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="f4a73-119">Questo comando controlla la compatibilità del sistema e anche di file e cartelle in C:\DATA.</span><span class="sxs-lookup"><span data-stu-id="f4a73-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="f4a73-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f4a73-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="f4a73-121">Questo comando controlla la compatibilità di file e cartelle in C:\DATA, ma non esegue un controllo di compatibilità del sistema.</span><span class="sxs-lookup"><span data-stu-id="f4a73-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="f4a73-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f4a73-122">Example 3</span></span>
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
```

<span data-ttu-id="f4a73-123">Questo comando controlla la compatibilità del sistema e anche di file e cartelle in C:\DATA e quindi Esporta i risultati come file CSV in C:\results.</span><span class="sxs-lookup"><span data-stu-id="f4a73-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="f4a73-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4a73-124">PARAMETERS</span></span>

### <span data-ttu-id="f4a73-125">-Nomecomputer</span><span class="sxs-lookup"><span data-stu-id="f4a73-125">-ComputerName</span></span>
<span data-ttu-id="f4a73-126">Il computer in cui si esegue l'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f4a73-126">The computer you are performing this check on.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a73-127">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="f4a73-127">-Credential</span></span>
<span data-ttu-id="f4a73-128">Le credenziali per la condivisione che si sta convalidando.</span><span class="sxs-lookup"><span data-stu-id="f4a73-128">Your credentials for the share you are validating.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a73-129">-Path</span><span class="sxs-lookup"><span data-stu-id="f4a73-129">-Path</span></span>
<span data-ttu-id="f4a73-130">Percorso UNC della condivisione che si sta convalidando.</span><span class="sxs-lookup"><span data-stu-id="f4a73-130">The UNC path of the share you are validating.</span></span>

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a73-131">-Silenzioso</span><span class="sxs-lookup"><span data-stu-id="f4a73-131">-Quiet</span></span>
<span data-ttu-id="f4a73-132">Elimina la scrittura di report di output in console.</span><span class="sxs-lookup"><span data-stu-id="f4a73-132">Suppresses writing output report to console.</span></span>

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

### <span data-ttu-id="f4a73-133">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="f4a73-133">-SkipNamespaceChecks</span></span>
<span data-ttu-id="f4a73-134">Imposta questo contrassegno per ignorare le convalide dello spazio dei nomi file e eseguire solo le convalide di sistema.</span><span class="sxs-lookup"><span data-stu-id="f4a73-134">Set this flag to skip file namespace validations and only perform system validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a73-135">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="f4a73-135">-SkipSystemChecks</span></span>
<span data-ttu-id="f4a73-136">Imposta questo contrassegno per ignorare le convalide di sistema e eseguire solo le convalide dello spazio dei nomi file.</span><span class="sxs-lookup"><span data-stu-id="f4a73-136">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="f4a73-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a73-137">CommonParameters</span></span>
<span data-ttu-id="f4a73-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4a73-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a73-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4a73-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a73-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4a73-140">INPUTS</span></span>

### <span data-ttu-id="f4a73-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f4a73-141">None</span></span>

## <span data-ttu-id="f4a73-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4a73-142">OUTPUTS</span></span>

### <span data-ttu-id="f4a73-143">Microsoft. Azure. Commands. StorageSync. Evaluation. Models. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="f4a73-143">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="f4a73-144">Note</span><span class="sxs-lookup"><span data-stu-id="f4a73-144">NOTES</span></span>
* <span data-ttu-id="f4a73-145">Parole chiave: Azure, azurerm, ARM, Resource, Management, StorageSync, filesync</span><span class="sxs-lookup"><span data-stu-id="f4a73-145">Keywords: azure, azurerm, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="f4a73-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4a73-146">RELATED LINKS</span></span>
