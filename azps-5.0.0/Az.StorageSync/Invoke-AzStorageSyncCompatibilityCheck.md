---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310500"
---
# <span data-ttu-id="98df3-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="98df3-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="98df3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98df3-102">SYNOPSIS</span></span>
<span data-ttu-id="98df3-103">Controlla i potenziali problemi di compatibilità tra il sistema e la sincronizzazione di file Azure.</span><span class="sxs-lookup"><span data-stu-id="98df3-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="98df3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98df3-104">SYNTAX</span></span>

### <span data-ttu-id="98df3-105">PathBased (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="98df3-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="98df3-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="98df3-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="98df3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98df3-107">DESCRIPTION</span></span>
<span data-ttu-id="98df3-108">Il cmdlet **Invoke-AzStorageSyncCompatibilityCheck** controlla i potenziali problemi di compatibilità tra il sistema e la sincronizzazione di file di Azure. Assegnato un percorso locale o remoto, esegue un set di convalide nello spazio dei nomi System e file e quindi restituisce i problemi di compatibilità che trova.</span><span class="sxs-lookup"><span data-stu-id="98df3-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="98df3-109">Controlli di sistema:</span><span class="sxs-lookup"><span data-stu-id="98df3-109">System checks:</span></span>
- <span data-ttu-id="98df3-110">Controlli dello spazio dei nomi del file di compatibilità OS:</span><span class="sxs-lookup"><span data-stu-id="98df3-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="98df3-111">Caratteri non supportati</span><span class="sxs-lookup"><span data-stu-id="98df3-111">Unsupported characters</span></span>
- <span data-ttu-id="98df3-112">Dimensione massima del file</span><span class="sxs-lookup"><span data-stu-id="98df3-112">Maximum file size</span></span>
- <span data-ttu-id="98df3-113">Lunghezza massima del percorso</span><span class="sxs-lookup"><span data-stu-id="98df3-113">Maximum path length</span></span>
- <span data-ttu-id="98df3-114">Lunghezza massima del file</span><span class="sxs-lookup"><span data-stu-id="98df3-114">Maximum file length</span></span>
- <span data-ttu-id="98df3-115">Dimensioni massime del set di dati</span><span class="sxs-lookup"><span data-stu-id="98df3-115">Maximum dataset size</span></span>
- <span data-ttu-id="98df3-116">Profondità massima della directory</span><span class="sxs-lookup"><span data-stu-id="98df3-116">Maximum directory depth</span></span>

## <span data-ttu-id="98df3-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98df3-117">EXAMPLES</span></span>

### <span data-ttu-id="98df3-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="98df3-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="98df3-119">Questo comando controlla la compatibilità del sistema e anche di file e cartelle in C:\DATA.</span><span class="sxs-lookup"><span data-stu-id="98df3-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="98df3-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="98df3-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="98df3-121">Questo comando controlla la compatibilità di file e cartelle in C:\DATA, ma non esegue un controllo di compatibilità del sistema.</span><span class="sxs-lookup"><span data-stu-id="98df3-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="98df3-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="98df3-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="98df3-123">Questo comando controlla la compatibilità del sistema e anche di file e cartelle in C:\DATA e quindi Esporta i risultati come file CSV in C:\results.</span><span class="sxs-lookup"><span data-stu-id="98df3-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="98df3-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98df3-124">PARAMETERS</span></span>

### <span data-ttu-id="98df3-125">-Nomecomputer</span><span class="sxs-lookup"><span data-stu-id="98df3-125">-ComputerName</span></span>
<span data-ttu-id="98df3-126">Il computer in cui si esegue l'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="98df3-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="98df3-127">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="98df3-127">-Credential</span></span>
<span data-ttu-id="98df3-128">Le credenziali per la condivisione che si sta convalidando.</span><span class="sxs-lookup"><span data-stu-id="98df3-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="98df3-129">-Path</span><span class="sxs-lookup"><span data-stu-id="98df3-129">-Path</span></span>
<span data-ttu-id="98df3-130">Percorso UNC della condivisione che si sta convalidando.</span><span class="sxs-lookup"><span data-stu-id="98df3-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="98df3-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="98df3-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="98df3-132">Imposta questo contrassegno per ignorare le convalide dello spazio dei nomi file e eseguire solo le convalide di sistema.</span><span class="sxs-lookup"><span data-stu-id="98df3-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="98df3-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="98df3-133">-SkipSystemChecks</span></span>
<span data-ttu-id="98df3-134">Imposta questo contrassegno per ignorare le convalide di sistema e eseguire solo le convalide dello spazio dei nomi file.</span><span class="sxs-lookup"><span data-stu-id="98df3-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="98df3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98df3-135">CommonParameters</span></span>
<span data-ttu-id="98df3-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98df3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98df3-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98df3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98df3-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98df3-138">INPUTS</span></span>

### <span data-ttu-id="98df3-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="98df3-139">None</span></span>

## <span data-ttu-id="98df3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98df3-140">OUTPUTS</span></span>

### <span data-ttu-id="98df3-141">Microsoft. Azure. Commands. StorageSync. Evaluation. Models. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="98df3-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="98df3-142">Note</span><span class="sxs-lookup"><span data-stu-id="98df3-142">NOTES</span></span>
* <span data-ttu-id="98df3-143">Parole chiave: Azure, AZ, ARM, Resource, Management, StorageSync, filesync</span><span class="sxs-lookup"><span data-stu-id="98df3-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="98df3-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98df3-144">RELATED LINKS</span></span>
