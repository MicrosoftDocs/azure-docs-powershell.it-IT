---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b51280387ad3eb29f05bee8876765a621e0d07c4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859638"
---
# <span data-ttu-id="03dae-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="03dae-101">Get-AzsBackup</span></span>

## <span data-ttu-id="03dae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03dae-102">SYNOPSIS</span></span>
<span data-ttu-id="03dae-103">Restituisce un backup da una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="03dae-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="03dae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03dae-104">SYNTAX</span></span>

### <span data-ttu-id="03dae-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="03dae-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="03dae-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="03dae-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="03dae-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="03dae-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="03dae-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="03dae-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="03dae-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03dae-109">DESCRIPTION</span></span>
<span data-ttu-id="03dae-110">Restituisce un backup da una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="03dae-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="03dae-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03dae-111">EXAMPLES</span></span>

### <span data-ttu-id="03dae-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="03dae-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="03dae-113">Ottenere informazioni sbout tutti i backup di Azure stack.</span><span class="sxs-lookup"><span data-stu-id="03dae-113">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="03dae-114">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="03dae-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="03dae-115">Ottenere informazioni per il backup dello stack di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="03dae-115">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="03dae-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03dae-116">PARAMETERS</span></span>

### <span data-ttu-id="03dae-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="03dae-117">-Location</span></span>
<span data-ttu-id="03dae-118">Eseguire il backup della posizione.</span><span class="sxs-lookup"><span data-stu-id="03dae-118">Location backed up.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03dae-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="03dae-119">-Name</span></span>
<span data-ttu-id="03dae-120">Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="03dae-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03dae-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="03dae-121">-ParentResource</span></span>
<span data-ttu-id="03dae-122">Il passaggio di un percorso di backup restituirà l'elenco di tutti i backup in tale posizione di backup.</span><span class="sxs-lookup"><span data-stu-id="03dae-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: ParentResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03dae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03dae-123">-ResourceGroupName</span></span>
<span data-ttu-id="03dae-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="03dae-124">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03dae-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03dae-125">-ResourceId</span></span>
<span data-ttu-id="03dae-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="03dae-126">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03dae-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="03dae-127">-Skip</span></span>
<span data-ttu-id="03dae-128">{{Fill Skip Description}}</span><span class="sxs-lookup"><span data-stu-id="03dae-128">{{Fill Skip Description}}</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03dae-129">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="03dae-129">-Top</span></span>
<span data-ttu-id="03dae-130">{{Fill Top Description}}</span><span class="sxs-lookup"><span data-stu-id="03dae-130">{{Fill Top Description}}</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03dae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03dae-131">CommonParameters</span></span>
<span data-ttu-id="03dae-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03dae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03dae-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03dae-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03dae-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03dae-134">INPUTS</span></span>

## <span data-ttu-id="03dae-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03dae-135">OUTPUTS</span></span>

### <span data-ttu-id="03dae-136">Microsoft. AzureStack. Management. backup. admin. Models. backup</span><span class="sxs-lookup"><span data-stu-id="03dae-136">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="03dae-137">Note</span><span class="sxs-lookup"><span data-stu-id="03dae-137">NOTES</span></span>

## <span data-ttu-id="03dae-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03dae-138">RELATED LINKS</span></span>

