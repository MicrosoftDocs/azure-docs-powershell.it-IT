---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 6b4527430fa74efa09aa07fd120d0acf8de0edfd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968478"
---
# <span data-ttu-id="00403-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="00403-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="00403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00403-102">SYNOPSIS</span></span>
<span data-ttu-id="00403-103">Crea un nuovo backup dei file ANF di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="00403-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="00403-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00403-104">SYNTAX</span></span>

### <span data-ttu-id="00403-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="00403-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00403-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00403-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00403-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="00403-107">DESCRIPTION</span></span>
<span data-ttu-id="00403-108">Il cmdlet **New-AzNetAppFilesBackup** crea un backup per un volume ANF.</span><span class="sxs-lookup"><span data-stu-id="00403-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="00403-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00403-109">EXAMPLES</span></span>

### <span data-ttu-id="00403-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="00403-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="00403-111">Questo comando crea il nuovo backup ANF per il volume denominato account "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="00403-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="00403-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00403-112">PARAMETERS</span></span>

### <span data-ttu-id="00403-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="00403-113">-AccountName</span></span>
<span data-ttu-id="00403-114">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="00403-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="00403-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00403-115">-DefaultProfile</span></span>
<span data-ttu-id="00403-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00403-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00403-117">-Label</span><span class="sxs-lookup"><span data-stu-id="00403-117">-Label</span></span>
<span data-ttu-id="00403-118">Etichetta per il backup</span><span class="sxs-lookup"><span data-stu-id="00403-118">Label for backup</span></span>

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

### <span data-ttu-id="00403-119">-Location</span><span class="sxs-lookup"><span data-stu-id="00403-119">-Location</span></span>
<span data-ttu-id="00403-120">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="00403-120">The location of the resource</span></span>

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

### <span data-ttu-id="00403-121">-Name</span><span class="sxs-lookup"><span data-stu-id="00403-121">-Name</span></span>
<span data-ttu-id="00403-122">Nome del backup ANF</span><span class="sxs-lookup"><span data-stu-id="00403-122">The name of the ANF backup</span></span>

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

### <span data-ttu-id="00403-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="00403-123">-PoolName</span></span>
<span data-ttu-id="00403-124">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="00403-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="00403-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00403-125">-ResourceGroupName</span></span>
<span data-ttu-id="00403-126">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="00403-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="00403-127">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="00403-127">-VolumeName</span></span>
<span data-ttu-id="00403-128">Nome del volume ANF</span><span class="sxs-lookup"><span data-stu-id="00403-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="00403-129">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="00403-129">-VolumeObject</span></span>
<span data-ttu-id="00403-130">Volume del nuovo oggetto di backup</span><span class="sxs-lookup"><span data-stu-id="00403-130">The volume for the new backup object</span></span>

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

### <span data-ttu-id="00403-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00403-131">-Confirm</span></span>
<span data-ttu-id="00403-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00403-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00403-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00403-133">-WhatIf</span></span>
<span data-ttu-id="00403-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00403-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00403-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00403-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00403-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00403-136">CommonParameters</span></span>
<span data-ttu-id="00403-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00403-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00403-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="00403-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00403-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="00403-139">INPUTS</span></span>

### <span data-ttu-id="00403-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="00403-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="00403-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00403-141">OUTPUTS</span></span>

### <span data-ttu-id="00403-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="00403-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="00403-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="00403-143">NOTES</span></span>

## <span data-ttu-id="00403-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00403-144">RELATED LINKS</span></span>
