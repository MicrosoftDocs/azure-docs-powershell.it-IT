---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 46f6f5d7f9d843a9dd6d30053e9205e52be989d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187287"
---
# <span data-ttu-id="2fc00-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="2fc00-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="2fc00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fc00-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc00-103">Recupera i dettagli di un backup dei file ANF di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="2fc00-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="2fc00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fc00-104">SYNTAX</span></span>

### <span data-ttu-id="2fc00-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2fc00-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fc00-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fc00-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fc00-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fc00-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fc00-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2fc00-108">DESCRIPTION</span></span>
<span data-ttu-id="2fc00-109">Il cmdlet **Get-AzNetAppFilesBackup** ottiene i dettagli di un backup ANF.</span><span class="sxs-lookup"><span data-stu-id="2fc00-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="2fc00-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fc00-110">EXAMPLES</span></span>

### <span data-ttu-id="2fc00-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2fc00-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="2fc00-112">Questo comando recupera il backcup denominato "MyAnfAccount" dal volume denominato "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="2fc00-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="2fc00-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fc00-113">PARAMETERS</span></span>

### <span data-ttu-id="2fc00-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2fc00-114">-AccountName</span></span>
<span data-ttu-id="2fc00-115">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="2fc00-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="2fc00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc00-116">-DefaultProfile</span></span>
<span data-ttu-id="2fc00-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2fc00-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fc00-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2fc00-118">-Name</span></span>
<span data-ttu-id="2fc00-119">Nome del backup ANF</span><span class="sxs-lookup"><span data-stu-id="2fc00-119">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc00-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2fc00-120">-PoolName</span></span>
<span data-ttu-id="2fc00-121">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="2fc00-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="2fc00-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fc00-122">-ResourceGroupName</span></span>
<span data-ttu-id="2fc00-123">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="2fc00-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="2fc00-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fc00-124">-ResourceId</span></span>
<span data-ttu-id="2fc00-125">ID risorsa del backup ANF</span><span class="sxs-lookup"><span data-stu-id="2fc00-125">The resource id of the ANF Backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc00-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="2fc00-126">-VolumeName</span></span>
<span data-ttu-id="2fc00-127">Nome del volume ANF</span><span class="sxs-lookup"><span data-stu-id="2fc00-127">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc00-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="2fc00-128">-VolumeObject</span></span>
<span data-ttu-id="2fc00-129">Oggetto volume contenente il backup da restituire</span><span class="sxs-lookup"><span data-stu-id="2fc00-129">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="2fc00-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc00-130">CommonParameters</span></span>
<span data-ttu-id="2fc00-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc00-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc00-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2fc00-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc00-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="2fc00-133">INPUTS</span></span>

### <span data-ttu-id="2fc00-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2fc00-134">System.String</span></span>

### <span data-ttu-id="2fc00-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2fc00-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="2fc00-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fc00-136">OUTPUTS</span></span>

### <span data-ttu-id="2fc00-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="2fc00-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="2fc00-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="2fc00-138">NOTES</span></span>

## <span data-ttu-id="2fc00-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fc00-139">RELATED LINKS</span></span>
