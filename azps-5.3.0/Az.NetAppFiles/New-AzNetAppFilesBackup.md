---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 66ba63b3e350093173ae9d1badc6c717a3c682aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474003"
---
# <span data-ttu-id="5781f-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="5781f-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="5781f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5781f-102">SYNOPSIS</span></span>
<span data-ttu-id="5781f-103">Crea un nuovo file di backup di Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="5781f-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="5781f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5781f-104">SYNTAX</span></span>

### <span data-ttu-id="5781f-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5781f-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5781f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5781f-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5781f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5781f-107">DESCRIPTION</span></span>
<span data-ttu-id="5781f-108">Il cmdlet **New-AzNetAppFilesBackup** crea un backup per un volume di ANF.</span><span class="sxs-lookup"><span data-stu-id="5781f-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="5781f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5781f-109">EXAMPLES</span></span>

### <span data-ttu-id="5781f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5781f-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="5781f-111">Questo comando crea il nuovo backup di ANF per il volume denominato account "volume".</span><span class="sxs-lookup"><span data-stu-id="5781f-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="5781f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5781f-112">PARAMETERS</span></span>

### <span data-ttu-id="5781f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5781f-113">-AccountName</span></span>
<span data-ttu-id="5781f-114">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="5781f-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="5781f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5781f-115">-DefaultProfile</span></span>
<span data-ttu-id="5781f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5781f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5781f-117">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="5781f-117">-Label</span></span>
<span data-ttu-id="5781f-118">Etichetta per il backup</span><span class="sxs-lookup"><span data-stu-id="5781f-118">Label for backup</span></span>

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

### <span data-ttu-id="5781f-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5781f-119">-Location</span></span>
<span data-ttu-id="5781f-120">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="5781f-120">The location of the resource</span></span>

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

### <span data-ttu-id="5781f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5781f-121">-Name</span></span>
<span data-ttu-id="5781f-122">Nome del backup di ANF</span><span class="sxs-lookup"><span data-stu-id="5781f-122">The name of the ANF backup</span></span>

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

### <span data-ttu-id="5781f-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="5781f-123">-PoolName</span></span>
<span data-ttu-id="5781f-124">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="5781f-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="5781f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5781f-125">-ResourceGroupName</span></span>
<span data-ttu-id="5781f-126">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="5781f-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="5781f-127">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="5781f-127">-VolumeName</span></span>
<span data-ttu-id="5781f-128">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="5781f-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="5781f-129">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="5781f-129">-VolumeObject</span></span>
<span data-ttu-id="5781f-130">Il volume per il nuovo oggetto di backup</span><span class="sxs-lookup"><span data-stu-id="5781f-130">The volume for the new backup object</span></span>

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

### <span data-ttu-id="5781f-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5781f-131">-Confirm</span></span>
<span data-ttu-id="5781f-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5781f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5781f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5781f-133">-WhatIf</span></span>
<span data-ttu-id="5781f-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5781f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5781f-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5781f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5781f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5781f-136">CommonParameters</span></span>
<span data-ttu-id="5781f-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5781f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5781f-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5781f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5781f-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5781f-139">INPUTS</span></span>

### <span data-ttu-id="5781f-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="5781f-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="5781f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5781f-141">OUTPUTS</span></span>

### <span data-ttu-id="5781f-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="5781f-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="5781f-143">Note</span><span class="sxs-lookup"><span data-stu-id="5781f-143">NOTES</span></span>

## <span data-ttu-id="5781f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5781f-144">RELATED LINKS</span></span>
