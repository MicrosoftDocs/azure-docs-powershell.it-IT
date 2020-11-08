---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 931BC75D-B8EF-463D-8FCE-A822093CB05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bbc1963dbf56d0ef7f31d2174ab352dcc36af619
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029666"
---
# <span data-ttu-id="c4471-101">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c4471-101">New-AzureStorageAccount</span></span>

## <span data-ttu-id="c4471-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4471-102">SYNOPSIS</span></span>
<span data-ttu-id="c4471-103">Crea un nuovo account di archiviazione in un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="c4471-103">Creates a new storage account in an Azure subscription.</span></span>

## <span data-ttu-id="c4471-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4471-104">SYNTAX</span></span>

### <span data-ttu-id="c4471-105">ParameterSetAffinityGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4471-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -AffinityGroup <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c4471-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="c4471-106">ParameterSetLocation</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -Location <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c4471-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4471-107">DESCRIPTION</span></span>
<span data-ttu-id="c4471-108">Il cmdlet **New-AzureStorageAccount** crea un account che fornisce l'accesso ai servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4471-108">The **New-AzureStorageAccount** cmdlet creates an account that provides access to Azure storage services.</span></span>
<span data-ttu-id="c4471-109">Un account di archiviazione è una risorsa univoca globale all'interno del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c4471-109">A storage account is a globally unique resource within the storage system.</span></span>
<span data-ttu-id="c4471-110">L'account è lo spazio dei nomi padre per i servizi BLOB, Queue e Table.</span><span class="sxs-lookup"><span data-stu-id="c4471-110">The account is the parent namespace for the Blob, Queue, and Table services.</span></span>

## <span data-ttu-id="c4471-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4471-111">EXAMPLES</span></span>

### <span data-ttu-id="c4471-112">Esempio 1: creare un account di archiviazione per un gruppo di affinità specificato</span><span class="sxs-lookup"><span data-stu-id="c4471-112">Example 1: Create a storage account for a specified affinity group</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure01" -Label "AzureOne" -AffinityGroup "prodapps"
```

<span data-ttu-id="c4471-113">Questo comando crea un account di archiviazione per un gruppo di affinità specificato.</span><span class="sxs-lookup"><span data-stu-id="c4471-113">This command creates a storage account for a specified affinity group.</span></span>

### <span data-ttu-id="c4471-114">Esempio 2: creare un account di archiviazione in una posizione specificata</span><span class="sxs-lookup"><span data-stu-id="c4471-114">Example 2: Create a storage account in a specified location</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure02" -Label "AzureTwo" -Location "North Central US"
```

<span data-ttu-id="c4471-115">Questo comando crea un account di archiviazione in una posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="c4471-115">This command creates a storage account in a specified location.</span></span>

## <span data-ttu-id="c4471-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4471-116">PARAMETERS</span></span>

### <span data-ttu-id="c4471-117">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="c4471-117">-AffinityGroup</span></span>
<span data-ttu-id="c4471-118">Specifica il nome di un gruppo di affinità esistente nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="c4471-118">Specifies the name of an existing affinity group in the current subscription.</span></span>
<span data-ttu-id="c4471-119">Puoi specificare il parametro *location* o *AffinityGroup* , ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="c4471-119">You can specify either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4471-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4471-120">-Description</span></span>
<span data-ttu-id="c4471-121">Specifica una descrizione per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c4471-121">Specifies a description for the storage account.</span></span>
<span data-ttu-id="c4471-122">La descrizione può contenere fino a 1024 caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="c4471-122">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4471-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c4471-123">-InformationAction</span></span>
<span data-ttu-id="c4471-124">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c4471-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c4471-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4471-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c4471-126">Continuare</span><span class="sxs-lookup"><span data-stu-id="c4471-126">Continue</span></span>
- <span data-ttu-id="c4471-127">Ignora</span><span class="sxs-lookup"><span data-stu-id="c4471-127">Ignore</span></span>
- <span data-ttu-id="c4471-128">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c4471-128">Inquire</span></span>
- <span data-ttu-id="c4471-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c4471-129">SilentlyContinue</span></span>
- <span data-ttu-id="c4471-130">Stop</span><span class="sxs-lookup"><span data-stu-id="c4471-130">Stop</span></span>
- <span data-ttu-id="c4471-131">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c4471-131">Suspend</span></span>

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

### <span data-ttu-id="c4471-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c4471-132">-InformationVariable</span></span>
<span data-ttu-id="c4471-133">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c4471-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c4471-134">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="c4471-134">-Label</span></span>
<span data-ttu-id="c4471-135">Specifica un'etichetta per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c4471-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="c4471-136">L'etichetta può contenere fino a 100 caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="c4471-136">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4471-137">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c4471-137">-Location</span></span>
<span data-ttu-id="c4471-138">Specifica la posizione del centro dati di Azure in cui viene creato l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c4471-138">Specifies the Azure data center location where the storage account is created.</span></span>
<span data-ttu-id="c4471-139">Puoi includere il parametro *location* o *AffinityGroup* , ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="c4471-139">You can include either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4471-140">-Profile</span><span class="sxs-lookup"><span data-stu-id="c4471-140">-Profile</span></span>
<span data-ttu-id="c4471-141">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4471-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4471-142">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c4471-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4471-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c4471-143">-StorageAccountName</span></span>
<span data-ttu-id="c4471-144">Specifica un nome per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c4471-144">Specifies a name for the storage account.</span></span>
<span data-ttu-id="c4471-145">Il nome dell'account di archiviazione deve essere univoco in Azure e deve avere una lunghezza compresa tra 3 e 24 caratteri e usare solo lettere minuscole e numeri.</span><span class="sxs-lookup"><span data-stu-id="c4471-145">The storage account name must be unique to Azure and must be between 3 and 24 characters in length and use lowercase letters and numbers only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4471-146">-Digitare</span><span class="sxs-lookup"><span data-stu-id="c4471-146">-Type</span></span>
<span data-ttu-id="c4471-147">Specifica il tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c4471-147">Specifies the type of the storage account.</span></span>
<span data-ttu-id="c4471-148">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="c4471-148">Valid values are:</span></span>

- <span data-ttu-id="c4471-149">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="c4471-149">Standard_LRS</span></span>
- <span data-ttu-id="c4471-150">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="c4471-150">Standard_ZRS</span></span>
- <span data-ttu-id="c4471-151">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="c4471-151">Standard_GRS</span></span>
- <span data-ttu-id="c4471-152">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="c4471-152">Standard_RAGRS</span></span>
- <span data-ttu-id="c4471-153">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="c4471-153">Premium_LRS</span></span>

<span data-ttu-id="c4471-154">Se questo parametro non viene specificato, il valore predefinito è Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="c4471-154">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="c4471-155">Gli account Standard_ZRS o Premium_LRS non possono essere modificati in altri tipi di account e viceversa.</span><span class="sxs-lookup"><span data-stu-id="c4471-155">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

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

### <span data-ttu-id="c4471-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4471-156">CommonParameters</span></span>
<span data-ttu-id="c4471-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4471-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4471-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4471-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4471-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4471-159">INPUTS</span></span>

## <span data-ttu-id="c4471-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4471-160">OUTPUTS</span></span>

## <span data-ttu-id="c4471-161">Note</span><span class="sxs-lookup"><span data-stu-id="c4471-161">NOTES</span></span>

## <span data-ttu-id="c4471-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4471-162">RELATED LINKS</span></span>

[<span data-ttu-id="c4471-163">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c4471-163">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="c4471-164">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c4471-164">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


