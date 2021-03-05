---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: b6052172ecca2821b1373d93a8de870969a6b4f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002206"
---
# <span data-ttu-id="9867d-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="9867d-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="9867d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9867d-102">SYNOPSIS</span></span>
<span data-ttu-id="9867d-103">Verifica la presenza di potenziali problemi di compatibilità tra il sistema e Azure File Sync.</span><span class="sxs-lookup"><span data-stu-id="9867d-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="9867d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9867d-104">SYNTAX</span></span>

### <span data-ttu-id="9867d-105">PathBased (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9867d-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="9867d-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="9867d-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="9867d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9867d-107">DESCRIPTION</span></span>
<span data-ttu-id="9867d-108">Il cmdlet **Invoke-AzStorageSyncCompatibilityCheck** verifica la presenza di potenziali problemi di compatibilità tra il sistema e Azure File Sync. In base a un percorso locale o remoto, esegue una serie di convalide sullo spazio dei nomi di sistema e file e quindi restituisce gli eventuali problemi di compatibilità rilevati.</span><span class="sxs-lookup"><span data-stu-id="9867d-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="9867d-109">Controlli di sistema:</span><span class="sxs-lookup"><span data-stu-id="9867d-109">System checks:</span></span>
- <span data-ttu-id="9867d-110">Controlli dello spazio dei nomi del file di compatibilità del sistema operativo:</span><span class="sxs-lookup"><span data-stu-id="9867d-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="9867d-111">Caratteri non supportati</span><span class="sxs-lookup"><span data-stu-id="9867d-111">Unsupported characters</span></span>
- <span data-ttu-id="9867d-112">Dimensioni massime del file</span><span class="sxs-lookup"><span data-stu-id="9867d-112">Maximum file size</span></span>
- <span data-ttu-id="9867d-113">Lunghezza massima del percorso</span><span class="sxs-lookup"><span data-stu-id="9867d-113">Maximum path length</span></span>
- <span data-ttu-id="9867d-114">Lunghezza massima dei file</span><span class="sxs-lookup"><span data-stu-id="9867d-114">Maximum file length</span></span>
- <span data-ttu-id="9867d-115">Dimensione massima del set di dati</span><span class="sxs-lookup"><span data-stu-id="9867d-115">Maximum dataset size</span></span>
- <span data-ttu-id="9867d-116">Profondità massima della directory</span><span class="sxs-lookup"><span data-stu-id="9867d-116">Maximum directory depth</span></span>

## <span data-ttu-id="9867d-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9867d-117">EXAMPLES</span></span>

### <span data-ttu-id="9867d-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9867d-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="9867d-119">Questo comando verifica la compatibilità del sistema e anche dei file e delle cartelle in C:\DATA.</span><span class="sxs-lookup"><span data-stu-id="9867d-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="9867d-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9867d-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="9867d-121">Questo comando verifica la compatibilità dei file e delle cartelle in C:\DATA, ma non esegue un controllo della compatibilità del sistema.</span><span class="sxs-lookup"><span data-stu-id="9867d-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="9867d-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9867d-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="9867d-123">Questo comando verifica la compatibilità del sistema e anche dei file e delle cartelle in C:\DATA e quindi esporta i risultati in un file CSV in C:\results.</span><span class="sxs-lookup"><span data-stu-id="9867d-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="9867d-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9867d-124">PARAMETERS</span></span>

### <span data-ttu-id="9867d-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="9867d-125">-ComputerName</span></span>
<span data-ttu-id="9867d-126">Computer in cui si sta eseguendo il controllo.</span><span class="sxs-lookup"><span data-stu-id="9867d-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="9867d-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="9867d-127">-Credential</span></span>
<span data-ttu-id="9867d-128">Le credenziali della condivisione che si sta convalidando.</span><span class="sxs-lookup"><span data-stu-id="9867d-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="9867d-129">-Path</span><span class="sxs-lookup"><span data-stu-id="9867d-129">-Path</span></span>
<span data-ttu-id="9867d-130">Percorso UNC della condivisione da convalidare.</span><span class="sxs-lookup"><span data-stu-id="9867d-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="9867d-131">-SkipCheckChecks</span><span class="sxs-lookup"><span data-stu-id="9867d-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="9867d-132">Impostare questo flag per ignorare le convalide degli spazi dei nomi file ed eseguire solo le convalide di sistema.</span><span class="sxs-lookup"><span data-stu-id="9867d-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="9867d-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="9867d-133">-SkipSystemChecks</span></span>
<span data-ttu-id="9867d-134">Impostare questo flag per ignorare le convalide di sistema ed eseguire solo le convalide degli spazi dei nomi file.</span><span class="sxs-lookup"><span data-stu-id="9867d-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="9867d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9867d-135">CommonParameters</span></span>
<span data-ttu-id="9867d-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9867d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9867d-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9867d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9867d-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="9867d-138">INPUTS</span></span>

### <span data-ttu-id="9867d-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9867d-139">None</span></span>

## <span data-ttu-id="9867d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9867d-140">OUTPUTS</span></span>

### <span data-ttu-id="9867d-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="9867d-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="9867d-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="9867d-142">NOTES</span></span>
* <span data-ttu-id="9867d-143">Parole chiave: azure, Az, arm, risorsa, gestione, storagesync, filesync</span><span class="sxs-lookup"><span data-stu-id="9867d-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="9867d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9867d-144">RELATED LINKS</span></span>
