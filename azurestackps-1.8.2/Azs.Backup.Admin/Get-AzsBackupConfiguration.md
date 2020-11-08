---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25091f0cb439e0447d19b534d59a0084a5b05c6e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030103"
---
# <span data-ttu-id="14634-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="14634-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="14634-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14634-102">SYNOPSIS</span></span>
<span data-ttu-id="14634-103">Restituisce l'elenco delle configurazioni di backup.</span><span class="sxs-lookup"><span data-stu-id="14634-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="14634-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14634-104">SYNTAX</span></span>

### <span data-ttu-id="14634-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14634-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="14634-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="14634-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="14634-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="14634-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="14634-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14634-108">DESCRIPTION</span></span>
<span data-ttu-id="14634-109">Restituisce l'elenco delle configurazioni di backup.</span><span class="sxs-lookup"><span data-stu-id="14634-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="14634-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14634-110">EXAMPLES</span></span>

### <span data-ttu-id="14634-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="14634-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="14634-112">Ottenere la configurazione di backup dello stack Azure.</span><span class="sxs-lookup"><span data-stu-id="14634-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="14634-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14634-113">PARAMETERS</span></span>

### <span data-ttu-id="14634-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="14634-114">-Location</span></span>
<span data-ttu-id="14634-115">Percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="14634-115">Backup location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14634-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14634-116">-ResourceGroupName</span></span>
<span data-ttu-id="14634-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="14634-117">Name of the resource group.</span></span>

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

### <span data-ttu-id="14634-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14634-118">-ResourceId</span></span>
<span data-ttu-id="14634-119">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="14634-119">The resource id.</span></span>

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

### <span data-ttu-id="14634-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="14634-120">-Skip</span></span>
<span data-ttu-id="14634-121">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="14634-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14634-122">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="14634-122">-Top</span></span>
<span data-ttu-id="14634-123">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="14634-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="14634-124">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="14634-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14634-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14634-125">CommonParameters</span></span>
<span data-ttu-id="14634-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14634-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14634-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14634-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14634-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14634-128">INPUTS</span></span>

## <span data-ttu-id="14634-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14634-129">OUTPUTS</span></span>

### <span data-ttu-id="14634-130">Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="14634-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="14634-131">Note</span><span class="sxs-lookup"><span data-stu-id="14634-131">NOTES</span></span>

## <span data-ttu-id="14634-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14634-132">RELATED LINKS</span></span>

