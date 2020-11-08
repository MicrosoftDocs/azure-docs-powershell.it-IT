---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AFD3971-460D-4F6A-B266-6ED98DC81CD4
online version: ''
schema: 2.0.0
ms.openlocfilehash: c007e3a318067f29da6ea710c25cf2c52d5df2b4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029701"
---
# <span data-ttu-id="c9100-101">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9100-101">Move-AzureStorageAccount</span></span>

## <span data-ttu-id="c9100-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9100-102">SYNOPSIS</span></span>
<span data-ttu-id="c9100-103">Esegue la migrazione di un account di archiviazione nello stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9100-103">Migrates a storage account to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="c9100-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9100-104">SYNTAX</span></span>

### <span data-ttu-id="c9100-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9100-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Validate] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c9100-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9100-106">AbortMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Abort] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c9100-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9100-107">CommitMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Commit] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c9100-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9100-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Prepare] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c9100-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9100-109">DESCRIPTION</span></span>
<span data-ttu-id="c9100-110">Il cmdlet **Move-AzureStorageAccount** esegue la migrazione di un account di archiviazione a un gruppo di risorse nello stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9100-110">The **Move-AzureStorageAccount** cmdlet migrates a storage account to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="c9100-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9100-111">EXAMPLES</span></span>

### <span data-ttu-id="c9100-112">Esempio 1: preparare la migrazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c9100-112">Example 1: Prepare storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Prepare -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="c9100-113">Questo comando prepara l'account di archiviazione denominato ContosoStorageName per la migrazione allo stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9100-113">This command prepares the storage account named ContosoStorageName for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="c9100-114">Esempio 2: avviare la migrazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c9100-114">Example 2: Start storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Commit -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="c9100-115">Questo comando avvia la migrazione dell'account di archiviazione denominato ContosoStorageName nello stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9100-115">This command starts migration of the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="c9100-116">Esempio 3: convalidare la migrazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c9100-116">Example 3: Validate storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Validate -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="c9100-117">Questo comando convalida la migrazione per l'account di archiviazione denominato ContosoStorageName nello stack di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9100-117">This command validates migration for the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="c9100-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9100-118">PARAMETERS</span></span>

### <span data-ttu-id="c9100-119">-Abort</span><span class="sxs-lookup"><span data-stu-id="c9100-119">-Abort</span></span>
<span data-ttu-id="c9100-120">Indica che questo cmdlet Annulla la migrazione dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c9100-120">Indicates that this cmdlet cancels the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9100-121">-Commit</span><span class="sxs-lookup"><span data-stu-id="c9100-121">-Commit</span></span>
<span data-ttu-id="c9100-122">Indica che questo cmdlet avvia la migrazione dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c9100-122">Indicates that this cmdlet starts the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9100-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c9100-123">-InformationAction</span></span>
<span data-ttu-id="c9100-124">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c9100-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c9100-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9100-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9100-126">Continuare</span><span class="sxs-lookup"><span data-stu-id="c9100-126">Continue</span></span>
- <span data-ttu-id="c9100-127">Ignora</span><span class="sxs-lookup"><span data-stu-id="c9100-127">Ignore</span></span>
- <span data-ttu-id="c9100-128">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c9100-128">Inquire</span></span>
- <span data-ttu-id="c9100-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c9100-129">SilentlyContinue</span></span>
- <span data-ttu-id="c9100-130">Stop</span><span class="sxs-lookup"><span data-stu-id="c9100-130">Stop</span></span>
- <span data-ttu-id="c9100-131">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c9100-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9100-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c9100-132">-InformationVariable</span></span>
<span data-ttu-id="c9100-133">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c9100-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9100-134">-Preparare</span><span class="sxs-lookup"><span data-stu-id="c9100-134">-Prepare</span></span>
<span data-ttu-id="c9100-135">Indica che questo cmdlet prepara l'account di archiviazione per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="c9100-135">Indicates that this cmdlet prepares the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9100-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="c9100-136">-Profile</span></span>
<span data-ttu-id="c9100-137">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9100-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c9100-138">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c9100-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9100-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c9100-139">-StorageAccountName</span></span>
<span data-ttu-id="c9100-140">Specifica il nome dell'account di archiviazione a cui viene eseguita la migrazione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9100-140">Specifies the name of the storage account that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9100-141">-Convalida</span><span class="sxs-lookup"><span data-stu-id="c9100-141">-Validate</span></span>
<span data-ttu-id="c9100-142">Specifica che questo cmdlet convalida l'account di archiviazione per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="c9100-142">Specifies that this cmdlet validates the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9100-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9100-143">CommonParameters</span></span>
<span data-ttu-id="c9100-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9100-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9100-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9100-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9100-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9100-146">INPUTS</span></span>

## <span data-ttu-id="c9100-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9100-147">OUTPUTS</span></span>

## <span data-ttu-id="c9100-148">Note</span><span class="sxs-lookup"><span data-stu-id="c9100-148">NOTES</span></span>

## <span data-ttu-id="c9100-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9100-149">RELATED LINKS</span></span>

[<span data-ttu-id="c9100-150">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c9100-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="c9100-151">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="c9100-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="c9100-152">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="c9100-152">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="c9100-153">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="c9100-153">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="c9100-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c9100-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


