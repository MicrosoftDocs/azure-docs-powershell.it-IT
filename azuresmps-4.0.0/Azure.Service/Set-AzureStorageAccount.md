---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023808"
---
# <span data-ttu-id="87ea6-101">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87ea6-101">Set-AzureStorageAccount</span></span>

## <span data-ttu-id="87ea6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="87ea6-103">Aggiorna le proprietà di un account di archiviazione in un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="87ea6-103">Updates the properties of a storage account in an Azure subscription.</span></span>

## <span data-ttu-id="87ea6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87ea6-104">SYNTAX</span></span>

### <span data-ttu-id="87ea6-105">AccountType (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="87ea6-105">AccountType (Default)</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="87ea6-106">GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="87ea6-106">GeoReplicationEnabled</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="87ea6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87ea6-107">DESCRIPTION</span></span>
<span data-ttu-id="87ea6-108">Il cmdlet **set-AzureStorageAccount** aggiorna le proprietà di un account di archiviazione di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="87ea6-108">The **Set-AzureStorageAccount** cmdlet updates the properties of an Azure storage account in the current subscription.</span></span>
<span data-ttu-id="87ea6-109">Le proprietà che è possibile impostare sono: **Label** , **Description** , **Type** e **GeoReplicationEnabled**.</span><span class="sxs-lookup"><span data-stu-id="87ea6-109">Properties that can be set are: **Label** , **Description** , **Type** and **GeoReplicationEnabled**.</span></span>

## <span data-ttu-id="87ea6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87ea6-110">EXAMPLES</span></span>

### <span data-ttu-id="87ea6-111">Esempio 1: aggiornare l'etichetta di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="87ea6-111">Example 1: Update the label for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

<span data-ttu-id="87ea6-112">Questo comando Aggiorna le proprietà **Label** e **Description** per l'account di archiviazione denominato ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="87ea6-112">This command updates the **Label** and **Description** properties for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="87ea6-113">Esempio 2: abilitare la Geo-replica per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="87ea6-113">Example 2: Enable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

<span data-ttu-id="87ea6-114">Questo comando imposta la proprietà **GeoReplicationEnabled** su $false per l'account di archiviazione denominato ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="87ea6-114">This command sets the **GeoReplicationEnabled** property to $False for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="87ea6-115">Esempio 3: disabilitare la Geo-replica per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="87ea6-115">Example 3: Disable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

<span data-ttu-id="87ea6-116">Questo comando imposta la proprietà **GeoReplicationEnabled** su $true per l'account di archiviazione denominato ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="87ea6-116">This command sets the **GeoReplicationEnabled** property to $True for the storage account named ContosoStorage01.</span></span>

## <span data-ttu-id="87ea6-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87ea6-117">PARAMETERS</span></span>

### <span data-ttu-id="87ea6-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="87ea6-118">-Description</span></span>
<span data-ttu-id="87ea6-119">Specifica una descrizione per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="87ea6-119">Specifies a description for the storage account.</span></span>
<span data-ttu-id="87ea6-120">La descrizione può contenere fino a 1024 caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="87ea6-120">The description may be up to 1024 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ea6-121">-GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="87ea6-121">-GeoReplicationEnabled</span></span>
<span data-ttu-id="87ea6-122">Specifica se l'account di archiviazione viene creato con la Geo-replica abilitata.</span><span class="sxs-lookup"><span data-stu-id="87ea6-122">Specifies whether the storage account is created with the geo-replication enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ea6-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="87ea6-123">-InformationAction</span></span>
<span data-ttu-id="87ea6-124">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="87ea6-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="87ea6-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="87ea6-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87ea6-126">Continuare</span><span class="sxs-lookup"><span data-stu-id="87ea6-126">Continue</span></span>
- <span data-ttu-id="87ea6-127">Ignora</span><span class="sxs-lookup"><span data-stu-id="87ea6-127">Ignore</span></span>
- <span data-ttu-id="87ea6-128">Informarsi</span><span class="sxs-lookup"><span data-stu-id="87ea6-128">Inquire</span></span>
- <span data-ttu-id="87ea6-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="87ea6-129">SilentlyContinue</span></span>
- <span data-ttu-id="87ea6-130">Stop</span><span class="sxs-lookup"><span data-stu-id="87ea6-130">Stop</span></span>
- <span data-ttu-id="87ea6-131">Sospensione</span><span class="sxs-lookup"><span data-stu-id="87ea6-131">Suspend</span></span>

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

### <span data-ttu-id="87ea6-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="87ea6-132">-InformationVariable</span></span>
<span data-ttu-id="87ea6-133">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="87ea6-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="87ea6-134">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="87ea6-134">-Label</span></span>
<span data-ttu-id="87ea6-135">Specifica un'etichetta per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="87ea6-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="87ea6-136">L'etichetta può contenere fino a 100 caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="87ea6-136">The label may be up to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ea6-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="87ea6-137">-Profile</span></span>
<span data-ttu-id="87ea6-138">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87ea6-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="87ea6-139">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="87ea6-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="87ea6-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="87ea6-140">-StorageAccountName</span></span>
<span data-ttu-id="87ea6-141">Specifica il nome dell'account di archiviazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87ea6-141">Specifies the name of the storage account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ea6-142">-Digitare</span><span class="sxs-lookup"><span data-stu-id="87ea6-142">-Type</span></span>
<span data-ttu-id="87ea6-143">Specifica il tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="87ea6-143">Specifies the type of the storage account.</span></span>
<span data-ttu-id="87ea6-144">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="87ea6-144">Valid values are:</span></span> 

- <span data-ttu-id="87ea6-145">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="87ea6-145">Standard_LRS</span></span>
- <span data-ttu-id="87ea6-146">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="87ea6-146">Standard_ZRS</span></span>
- <span data-ttu-id="87ea6-147">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="87ea6-147">Standard_GRS</span></span>
- <span data-ttu-id="87ea6-148">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="87ea6-148">Standard_RAGRS</span></span>
- <span data-ttu-id="87ea6-149">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="87ea6-149">Premium_LRS</span></span>

<span data-ttu-id="87ea6-150">Se questo parametro non viene specificato, il valore predefinito è Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="87ea6-150">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="87ea6-151">L'effetto di specificare il parametro *GeoReplicationEnabled* è lo stesso che specificare Standard_GRS nel parametro di *tipo* .</span><span class="sxs-lookup"><span data-stu-id="87ea6-151">The effect of specifying the *GeoReplicationEnabled* parameter is the same as specifying Standard_GRS in the *Type* parameter.</span></span>

<span data-ttu-id="87ea6-152">Gli account Standard_ZRS o Premium_LRS non possono essere modificati in altri tipi di account e viceversa.</span><span class="sxs-lookup"><span data-stu-id="87ea6-152">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

```yaml
Type: String
Parameter Sets: AccountType
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ea6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ea6-153">CommonParameters</span></span>
<span data-ttu-id="87ea6-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87ea6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ea6-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87ea6-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ea6-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87ea6-156">INPUTS</span></span>

## <span data-ttu-id="87ea6-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87ea6-157">OUTPUTS</span></span>

## <span data-ttu-id="87ea6-158">Note</span><span class="sxs-lookup"><span data-stu-id="87ea6-158">NOTES</span></span>

## <span data-ttu-id="87ea6-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87ea6-159">RELATED LINKS</span></span>

[<span data-ttu-id="87ea6-160">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87ea6-160">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="87ea6-161">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87ea6-161">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="87ea6-162">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87ea6-162">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)


