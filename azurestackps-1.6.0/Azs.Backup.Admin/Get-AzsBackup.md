---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb306ed03cb9ab1f06209345474b2ef196d9e1d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93506976"
---
# <span data-ttu-id="9b723-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="9b723-101">Get-AzsBackup</span></span>

## <span data-ttu-id="9b723-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b723-102">SYNOPSIS</span></span>
<span data-ttu-id="9b723-103">Restituisce un backup da una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="9b723-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="9b723-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b723-104">SYNTAX</span></span>

### <span data-ttu-id="9b723-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9b723-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b723-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="9b723-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9b723-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b723-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="9b723-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="9b723-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9b723-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b723-109">DESCRIPTION</span></span>
<span data-ttu-id="9b723-110">Restituisce un backup da una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="9b723-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="9b723-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b723-111">EXAMPLES</span></span>

### <span data-ttu-id="9b723-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9b723-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="9b723-113">Ottenere informazioni su tutti i backup di Azure stack.</span><span class="sxs-lookup"><span data-stu-id="9b723-113">Get information about all Azure Stack backups.</span></span>

### <span data-ttu-id="9b723-114">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9b723-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="9b723-115">Ottenere informazioni per il backup dello stack di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="9b723-115">Get information for the specified Azure Stack backup.</span></span>

## <span data-ttu-id="9b723-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b723-116">PARAMETERS</span></span>

### <span data-ttu-id="9b723-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9b723-117">-Location</span></span>
<span data-ttu-id="9b723-118">Eseguire il backup della posizione.</span><span class="sxs-lookup"><span data-stu-id="9b723-118">Location backed up.</span></span>

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

### <span data-ttu-id="9b723-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b723-119">-Name</span></span>
<span data-ttu-id="9b723-120">Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="9b723-120">Name of the backup.</span></span>

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

### <span data-ttu-id="9b723-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="9b723-121">-ParentResource</span></span>
<span data-ttu-id="9b723-122">Il passaggio di un percorso di backup restituirà l'elenco di tutti i backup in tale posizione di backup.</span><span class="sxs-lookup"><span data-stu-id="9b723-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

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

### <span data-ttu-id="9b723-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b723-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b723-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9b723-124">Name of the resource group.</span></span>

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

### <span data-ttu-id="9b723-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b723-125">-ResourceId</span></span>
<span data-ttu-id="9b723-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9b723-126">The resource id.</span></span>

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

### <span data-ttu-id="9b723-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="9b723-127">-Skip</span></span>
<span data-ttu-id="9b723-128">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="9b723-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9b723-129">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="9b723-129">-Top</span></span>
<span data-ttu-id="9b723-130">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="9b723-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9b723-131">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="9b723-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9b723-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b723-132">CommonParameters</span></span>
<span data-ttu-id="9b723-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b723-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b723-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b723-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b723-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b723-135">INPUTS</span></span>

## <span data-ttu-id="9b723-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b723-136">OUTPUTS</span></span>

### <span data-ttu-id="9b723-137">Microsoft. AzureStack. Management. backup. admin. Models. backup</span><span class="sxs-lookup"><span data-stu-id="9b723-137">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="9b723-138">Note</span><span class="sxs-lookup"><span data-stu-id="9b723-138">NOTES</span></span>

## <span data-ttu-id="9b723-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b723-139">RELATED LINKS</span></span>

