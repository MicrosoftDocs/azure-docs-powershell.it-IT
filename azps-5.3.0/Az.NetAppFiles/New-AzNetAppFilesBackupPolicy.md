---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: ce49a011ba7e6c746c97e4b1aca6273d7d8b650d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473999"
---
# <span data-ttu-id="4db77-101">New-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4db77-101">New-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="4db77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4db77-102">SYNOPSIS</span></span>
<span data-ttu-id="4db77-103">Crea un nuovo criterio di backup di Azure NetApp Files (ANF) per un account ANF.</span><span class="sxs-lookup"><span data-stu-id="4db77-103">Creates a new Azure NetApp Files (ANF) backup policy for an ANF account.</span></span>

## <span data-ttu-id="4db77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4db77-104">SYNTAX</span></span>

### <span data-ttu-id="4db77-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4db77-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4db77-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4db77-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackupPolicy -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>]
 [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4db77-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4db77-107">DESCRIPTION</span></span>
<span data-ttu-id="4db77-108">Il cmdlet **New-AzNetAppFilesActiveDirectory** crea un nuovo criterio di backup per un account di ANF.</span><span class="sxs-lookup"><span data-stu-id="4db77-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new backup policy for an ANF account.</span></span>

## <span data-ttu-id="4db77-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4db77-109">EXAMPLES</span></span>

### <span data-ttu-id="4db77-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4db77-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyBackupPolicy" -Tag @{"tag1" = "tagValue"} -Enabled -DailyBackupsToKeep 1 -WeeklyBackupsToKeep 2 -MonthlyBackupsToKeep 2 -YearlyBackupsToKeep 1
```

<span data-ttu-id="4db77-111">Questo comando crea il nuovo criterio di backup di ANF per l'account ANF denominato account "account".</span><span class="sxs-lookup"><span data-stu-id="4db77-111">This command creates the new ANF backup policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="4db77-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4db77-112">PARAMETERS</span></span>

### <span data-ttu-id="4db77-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4db77-113">-AccountName</span></span>
<span data-ttu-id="4db77-114">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="4db77-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="4db77-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="4db77-115">-AccountObject</span></span>
<span data-ttu-id="4db77-116">Oggetto account per i nuovi criteri di backup</span><span class="sxs-lookup"><span data-stu-id="4db77-116">The Account object for the new Backup Policy</span></span>

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

### <span data-ttu-id="4db77-117">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="4db77-117">-DailyBackupsToKeep</span></span>
<span data-ttu-id="4db77-118">Conteggio backup giornalieri da conservare</span><span class="sxs-lookup"><span data-stu-id="4db77-118">Daily backups count to keep</span></span>

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

### <span data-ttu-id="4db77-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db77-119">-DefaultProfile</span></span>
<span data-ttu-id="4db77-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4db77-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4db77-121">-Enabled</span><span class="sxs-lookup"><span data-stu-id="4db77-121">-Enabled</span></span>
<span data-ttu-id="4db77-122">La proprietà per decidere i criteri è abilitata o meno</span><span class="sxs-lookup"><span data-stu-id="4db77-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="4db77-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4db77-123">-Location</span></span>
<span data-ttu-id="4db77-124">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="4db77-124">The location of the resource</span></span>

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

### <span data-ttu-id="4db77-125">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="4db77-125">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="4db77-126">Numero di backup mensili da conservare</span><span class="sxs-lookup"><span data-stu-id="4db77-126">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="4db77-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="4db77-127">-Name</span></span>
<span data-ttu-id="4db77-128">Nome del criterio di backup di ANF</span><span class="sxs-lookup"><span data-stu-id="4db77-128">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="4db77-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4db77-129">-ResourceGroupName</span></span>
<span data-ttu-id="4db77-130">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="4db77-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="4db77-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="4db77-131">-Tag</span></span>
<span data-ttu-id="4db77-132">Matrice Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="4db77-132">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="4db77-133">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="4db77-133">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="4db77-134">Conteggio backup settimanali da conservare</span><span class="sxs-lookup"><span data-stu-id="4db77-134">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="4db77-135">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="4db77-135">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="4db77-136">Numero di copie di backup annuali da conservare</span><span class="sxs-lookup"><span data-stu-id="4db77-136">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="4db77-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4db77-137">-Confirm</span></span>
<span data-ttu-id="4db77-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4db77-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4db77-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4db77-139">-WhatIf</span></span>
<span data-ttu-id="4db77-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4db77-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4db77-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4db77-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4db77-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db77-142">CommonParameters</span></span>
<span data-ttu-id="4db77-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4db77-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db77-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4db77-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db77-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4db77-145">INPUTS</span></span>

### <span data-ttu-id="4db77-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4db77-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="4db77-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4db77-147">OUTPUTS</span></span>

### <span data-ttu-id="4db77-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4db77-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="4db77-149">Note</span><span class="sxs-lookup"><span data-stu-id="4db77-149">NOTES</span></span>

## <span data-ttu-id="4db77-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4db77-150">RELATED LINKS</span></span>
