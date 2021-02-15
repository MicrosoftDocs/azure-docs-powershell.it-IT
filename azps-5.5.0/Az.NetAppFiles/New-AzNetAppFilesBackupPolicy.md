---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: ce49a011ba7e6c746c97e4b1aca6273d7d8b650d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203318"
---
# <span data-ttu-id="bbd39-101">New-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="bbd39-101">New-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="bbd39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbd39-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd39-103">Crea un nuovo criterio di backup dei file ANF di Azure NetApp per un account ANF.</span><span class="sxs-lookup"><span data-stu-id="bbd39-103">Creates a new Azure NetApp Files (ANF) backup policy for an ANF account.</span></span>

## <span data-ttu-id="bbd39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbd39-104">SYNTAX</span></span>

### <span data-ttu-id="bbd39-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bbd39-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbd39-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbd39-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackupPolicy -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>]
 [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbd39-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bbd39-107">DESCRIPTION</span></span>
<span data-ttu-id="bbd39-108">Il cmdlet **New-AzNetAppFilesActiveDirectory** crea un nuovo criterio di backup per un account ANF.</span><span class="sxs-lookup"><span data-stu-id="bbd39-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new backup policy for an ANF account.</span></span>

## <span data-ttu-id="bbd39-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbd39-109">EXAMPLES</span></span>

### <span data-ttu-id="bbd39-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bbd39-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyBackupPolicy" -Tag @{"tag1" = "tagValue"} -Enabled -DailyBackupsToKeep 1 -WeeklyBackupsToKeep 2 -MonthlyBackupsToKeep 2 -YearlyBackupsToKeep 1
```

<span data-ttu-id="bbd39-111">Questo comando crea il nuovo criterio di backup ANF per l'account ANF denominato account "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="bbd39-111">This command creates the new ANF backup policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="bbd39-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbd39-112">PARAMETERS</span></span>

### <span data-ttu-id="bbd39-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bbd39-113">-AccountName</span></span>
<span data-ttu-id="bbd39-114">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="bbd39-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="bbd39-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="bbd39-115">-AccountObject</span></span>
<span data-ttu-id="bbd39-116">Oggetto Account per il nuovo criterio di backup</span><span class="sxs-lookup"><span data-stu-id="bbd39-116">The Account object for the new Backup Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbd39-117">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="bbd39-117">-DailyBackupsToKeep</span></span>
<span data-ttu-id="bbd39-118">I backup giornalieri sono da conservare</span><span class="sxs-lookup"><span data-stu-id="bbd39-118">Daily backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd39-119">-DefaultProfile</span></span>
<span data-ttu-id="bbd39-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd39-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbd39-121">-Enabled</span><span class="sxs-lookup"><span data-stu-id="bbd39-121">-Enabled</span></span>
<span data-ttu-id="bbd39-122">La proprietà per decidere i criteri è abilitata o meno</span><span class="sxs-lookup"><span data-stu-id="bbd39-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="bbd39-123">-Location</span><span class="sxs-lookup"><span data-stu-id="bbd39-123">-Location</span></span>
<span data-ttu-id="bbd39-124">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="bbd39-124">The location of the resource</span></span>

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

### <span data-ttu-id="bbd39-125">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="bbd39-125">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="bbd39-126">Conteggio dei backup mensili da conservare</span><span class="sxs-lookup"><span data-stu-id="bbd39-126">Monthly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd39-127">-Name</span><span class="sxs-lookup"><span data-stu-id="bbd39-127">-Name</span></span>
<span data-ttu-id="bbd39-128">Nome dei criteri di backup ANF</span><span class="sxs-lookup"><span data-stu-id="bbd39-128">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd39-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbd39-129">-ResourceGroupName</span></span>
<span data-ttu-id="bbd39-130">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="bbd39-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="bbd39-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="bbd39-131">-Tag</span></span>
<span data-ttu-id="bbd39-132">Matrice di tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="bbd39-132">A hashtable array which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd39-133">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="bbd39-133">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="bbd39-134">Conteggio dei backup settimanali da conservare</span><span class="sxs-lookup"><span data-stu-id="bbd39-134">Weekly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd39-135">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="bbd39-135">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="bbd39-136">Numero di backup annuale da conservare</span><span class="sxs-lookup"><span data-stu-id="bbd39-136">Yearly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd39-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbd39-137">-Confirm</span></span>
<span data-ttu-id="bbd39-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbd39-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbd39-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbd39-139">-WhatIf</span></span>
<span data-ttu-id="bbd39-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbd39-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbd39-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbd39-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbd39-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd39-142">CommonParameters</span></span>
<span data-ttu-id="bbd39-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbd39-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd39-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bbd39-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd39-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="bbd39-145">INPUTS</span></span>

### <span data-ttu-id="bbd39-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bbd39-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="bbd39-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbd39-147">OUTPUTS</span></span>

### <span data-ttu-id="bbd39-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="bbd39-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="bbd39-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="bbd39-149">NOTES</span></span>

## <span data-ttu-id="bbd39-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbd39-150">RELATED LINKS</span></span>
