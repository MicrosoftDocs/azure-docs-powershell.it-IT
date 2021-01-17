---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 46f6f5d7f9d843a9dd6d30053e9205e52be989d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360093"
---
# <span data-ttu-id="52676-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="52676-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="52676-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52676-102">SYNOPSIS</span></span>
<span data-ttu-id="52676-103">Ottiene i dettagli di un backup di Azure NetApp file (ANF).</span><span class="sxs-lookup"><span data-stu-id="52676-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="52676-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52676-104">SYNTAX</span></span>

### <span data-ttu-id="52676-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52676-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52676-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52676-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52676-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52676-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52676-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52676-108">DESCRIPTION</span></span>
<span data-ttu-id="52676-109">Il cmdlet **Get-AzNetAppFilesBackup** ottiene i dettagli di un backup di ANF.</span><span class="sxs-lookup"><span data-stu-id="52676-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="52676-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52676-110">EXAMPLES</span></span>

### <span data-ttu-id="52676-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="52676-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="52676-112">Questo comando ottiene il backcup denominato "MyAnfAccount" dal volume denominato "volume".</span><span class="sxs-lookup"><span data-stu-id="52676-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="52676-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52676-113">PARAMETERS</span></span>

### <span data-ttu-id="52676-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="52676-114">-AccountName</span></span>
<span data-ttu-id="52676-115">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="52676-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="52676-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52676-116">-DefaultProfile</span></span>
<span data-ttu-id="52676-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52676-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52676-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="52676-118">-Name</span></span>
<span data-ttu-id="52676-119">Nome del backup di ANF</span><span class="sxs-lookup"><span data-stu-id="52676-119">The name of the ANF backup</span></span>

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

### <span data-ttu-id="52676-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="52676-120">-PoolName</span></span>
<span data-ttu-id="52676-121">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="52676-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="52676-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52676-122">-ResourceGroupName</span></span>
<span data-ttu-id="52676-123">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="52676-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="52676-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52676-124">-ResourceId</span></span>
<span data-ttu-id="52676-125">ID risorsa del backup di ANF</span><span class="sxs-lookup"><span data-stu-id="52676-125">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="52676-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="52676-126">-VolumeName</span></span>
<span data-ttu-id="52676-127">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="52676-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="52676-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="52676-128">-VolumeObject</span></span>
<span data-ttu-id="52676-129">Oggetto volume contenente il backup da restituire</span><span class="sxs-lookup"><span data-stu-id="52676-129">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="52676-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52676-130">CommonParameters</span></span>
<span data-ttu-id="52676-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52676-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52676-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52676-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52676-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52676-133">INPUTS</span></span>

### <span data-ttu-id="52676-134">System. String</span><span class="sxs-lookup"><span data-stu-id="52676-134">System.String</span></span>

### <span data-ttu-id="52676-135">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="52676-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="52676-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52676-136">OUTPUTS</span></span>

### <span data-ttu-id="52676-137">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="52676-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="52676-138">Note</span><span class="sxs-lookup"><span data-stu-id="52676-138">NOTES</span></span>

## <span data-ttu-id="52676-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52676-139">RELATED LINKS</span></span>
