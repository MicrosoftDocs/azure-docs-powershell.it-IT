---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcbc31b31558a38e61648a0eb9318f68daf19d2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491053"
---
# <span data-ttu-id="ee944-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="ee944-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="ee944-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee944-102">SYNOPSIS</span></span>
<span data-ttu-id="ee944-103">Avvia un processo di migrazione del disco gestito per eseguire la migrazione dei dischi gestiti alla condivisione di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="ee944-103">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

## <span data-ttu-id="ee944-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee944-104">SYNTAX</span></span>

```
New-AzsDiskMigrationJob [-Disks] <Disk[]> [-TargetShare] <String> [[-Location] <String>] [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="ee944-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee944-105">DESCRIPTION</span></span>
<span data-ttu-id="ee944-106">Creare un processo di migrazione disco.</span><span class="sxs-lookup"><span data-stu-id="ee944-106">Create a disk migration job.</span></span>

## <span data-ttu-id="ee944-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee944-107">EXAMPLES</span></span>

### <span data-ttu-id="ee944-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ee944-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDiskMigrationJob -Name "MyMigrationJob" -Disks $disks -location local -TargetShare "\\SU1FileServer.azurestack.local\SU1_ObjStore"
```

<span data-ttu-id="ee944-109">Avviare un processo di migrazione su disco gestito per i primi 20 dischi</span><span class="sxs-lookup"><span data-stu-id="ee944-109">Start a managed disk migration job for the first 20 disks</span></span>

## <span data-ttu-id="ee944-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee944-110">PARAMETERS</span></span>

### <span data-ttu-id="ee944-111">-Dischi</span><span class="sxs-lookup"><span data-stu-id="ee944-111">-Disks</span></span>
<span data-ttu-id="ee944-112">I parametri dell'elenco dei dischi.</span><span class="sxs-lookup"><span data-stu-id="ee944-112">The parameters of disk list.</span></span>

```yaml
Type: Disk[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee944-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ee944-113">-Location</span></span>
<span data-ttu-id="ee944-114">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ee944-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee944-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee944-115">-Name</span></span>
<span data-ttu-id="ee944-116">Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="ee944-116">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee944-117">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="ee944-117">-TargetShare</span></span>
<span data-ttu-id="ee944-118">Nome della condivisione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ee944-118">The target share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee944-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee944-119">CommonParameters</span></span>
<span data-ttu-id="ee944-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee944-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee944-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee944-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee944-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee944-122">INPUTS</span></span>

## <span data-ttu-id="ee944-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee944-123">OUTPUTS</span></span>

### <span data-ttu-id="ee944-124">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="ee944-124">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="ee944-125">Note</span><span class="sxs-lookup"><span data-stu-id="ee944-125">NOTES</span></span>

## <span data-ttu-id="ee944-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee944-126">RELATED LINKS</span></span>

