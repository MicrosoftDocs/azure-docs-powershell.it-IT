---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 8a4183c148eda0f5f560d24c2b5874ff5577e85e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968637"
---
# <span data-ttu-id="fe19e-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="fe19e-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="fe19e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe19e-102">SYNOPSIS</span></span>
<span data-ttu-id="fe19e-103">Recupera i dettagli di un backup dei file ANF di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="fe19e-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="fe19e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe19e-104">SYNTAX</span></span>

### <span data-ttu-id="fe19e-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fe19e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe19e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe19e-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe19e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe19e-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe19e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fe19e-108">DESCRIPTION</span></span>
<span data-ttu-id="fe19e-109">Il cmdlet **Get-AzNetAppFilesBackup** ottiene i dettagli di un backup ANF.</span><span class="sxs-lookup"><span data-stu-id="fe19e-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="fe19e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe19e-110">EXAMPLES</span></span>

### <span data-ttu-id="fe19e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fe19e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="fe19e-112">Questo comando recupera il backcup denominato "MyAnfAccount" dal volume denominato "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="fe19e-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="fe19e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe19e-113">PARAMETERS</span></span>

### <span data-ttu-id="fe19e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fe19e-114">-AccountName</span></span>
<span data-ttu-id="fe19e-115">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="fe19e-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="fe19e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe19e-116">-DefaultProfile</span></span>
<span data-ttu-id="fe19e-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe19e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe19e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fe19e-118">-Name</span></span>
<span data-ttu-id="fe19e-119">Nome del backup ANF</span><span class="sxs-lookup"><span data-stu-id="fe19e-119">The name of the ANF backup</span></span>

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

### <span data-ttu-id="fe19e-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="fe19e-120">-PoolName</span></span>
<span data-ttu-id="fe19e-121">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="fe19e-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="fe19e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe19e-122">-ResourceGroupName</span></span>
<span data-ttu-id="fe19e-123">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="fe19e-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="fe19e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe19e-124">-ResourceId</span></span>
<span data-ttu-id="fe19e-125">ID risorsa del backup ANF</span><span class="sxs-lookup"><span data-stu-id="fe19e-125">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="fe19e-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="fe19e-126">-VolumeName</span></span>
<span data-ttu-id="fe19e-127">Nome del volume ANF</span><span class="sxs-lookup"><span data-stu-id="fe19e-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="fe19e-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="fe19e-128">-VolumeObject</span></span>
<span data-ttu-id="fe19e-129">Oggetto volume contenente il backup da restituire</span><span class="sxs-lookup"><span data-stu-id="fe19e-129">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="fe19e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe19e-130">CommonParameters</span></span>
<span data-ttu-id="fe19e-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe19e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe19e-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fe19e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe19e-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="fe19e-133">INPUTS</span></span>

### <span data-ttu-id="fe19e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fe19e-134">System.String</span></span>

### <span data-ttu-id="fe19e-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="fe19e-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="fe19e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe19e-136">OUTPUTS</span></span>

### <span data-ttu-id="fe19e-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="fe19e-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="fe19e-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="fe19e-138">NOTES</span></span>

## <span data-ttu-id="fe19e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe19e-139">RELATED LINKS</span></span>
