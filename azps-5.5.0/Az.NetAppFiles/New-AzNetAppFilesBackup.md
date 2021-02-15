---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 66ba63b3e350093173ae9d1badc6c717a3c682aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184847"
---
# <span data-ttu-id="b0bbd-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="b0bbd-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="b0bbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="b0bbd-103">Crea un nuovo backup dei file ANF di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="b0bbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0bbd-104">SYNTAX</span></span>

### <span data-ttu-id="b0bbd-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0bbd-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0bbd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0bbd-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0bbd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b0bbd-107">DESCRIPTION</span></span>
<span data-ttu-id="b0bbd-108">Il cmdlet **New-AzNetAppFilesBackup** crea un backup per un volume ANF.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="b0bbd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0bbd-109">EXAMPLES</span></span>

### <span data-ttu-id="b0bbd-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b0bbd-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="b0bbd-111">Questo comando crea il nuovo backup ANF per il volume denominato account "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="b0bbd-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="b0bbd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0bbd-112">PARAMETERS</span></span>

### <span data-ttu-id="b0bbd-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b0bbd-113">-AccountName</span></span>
<span data-ttu-id="b0bbd-114">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="b0bbd-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="b0bbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0bbd-115">-DefaultProfile</span></span>
<span data-ttu-id="b0bbd-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0bbd-117">-Label</span><span class="sxs-lookup"><span data-stu-id="b0bbd-117">-Label</span></span>
<span data-ttu-id="b0bbd-118">Etichetta per il backup</span><span class="sxs-lookup"><span data-stu-id="b0bbd-118">Label for backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0bbd-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b0bbd-119">-Location</span></span>
<span data-ttu-id="b0bbd-120">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="b0bbd-120">The location of the resource</span></span>

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

### <span data-ttu-id="b0bbd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b0bbd-121">-Name</span></span>
<span data-ttu-id="b0bbd-122">Nome del backup ANF</span><span class="sxs-lookup"><span data-stu-id="b0bbd-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0bbd-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b0bbd-123">-PoolName</span></span>
<span data-ttu-id="b0bbd-124">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="b0bbd-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="b0bbd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0bbd-125">-ResourceGroupName</span></span>
<span data-ttu-id="b0bbd-126">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="b0bbd-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b0bbd-127">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="b0bbd-127">-VolumeName</span></span>
<span data-ttu-id="b0bbd-128">Nome del volume ANF</span><span class="sxs-lookup"><span data-stu-id="b0bbd-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="b0bbd-129">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="b0bbd-129">-VolumeObject</span></span>
<span data-ttu-id="b0bbd-130">Volume del nuovo oggetto di backup</span><span class="sxs-lookup"><span data-stu-id="b0bbd-130">The volume for the new backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0bbd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0bbd-131">-Confirm</span></span>
<span data-ttu-id="b0bbd-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0bbd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0bbd-133">-WhatIf</span></span>
<span data-ttu-id="b0bbd-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0bbd-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0bbd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0bbd-136">CommonParameters</span></span>
<span data-ttu-id="b0bbd-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0bbd-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b0bbd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0bbd-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="b0bbd-139">INPUTS</span></span>

### <span data-ttu-id="b0bbd-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b0bbd-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b0bbd-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0bbd-141">OUTPUTS</span></span>

### <span data-ttu-id="b0bbd-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="b0bbd-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="b0bbd-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="b0bbd-143">NOTES</span></span>

## <span data-ttu-id="b0bbd-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0bbd-144">RELATED LINKS</span></span>
