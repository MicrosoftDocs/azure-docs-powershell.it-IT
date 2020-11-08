---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023507"
---
# <span data-ttu-id="06997-101">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="06997-101">Get-AzureStorageAccount</span></span>

## <span data-ttu-id="06997-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06997-102">SYNOPSIS</span></span>
<span data-ttu-id="06997-103">Ottiene gli account di archiviazione per l'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="06997-103">Gets the storage accounts for the current Azure subscription.</span></span>

## <span data-ttu-id="06997-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06997-104">SYNTAX</span></span>

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="06997-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06997-105">DESCRIPTION</span></span>
<span data-ttu-id="06997-106">Il cmdlet **Get-AzureStorageAccount** restituisce un oggetto che contiene informazioni sugli account di archiviazione per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="06997-106">The **Get-AzureStorageAccount** cmdlet returns an object containing information about the storage accounts for the current subscription.</span></span>
<span data-ttu-id="06997-107">Se viene specificato il parametro *StorageAccountName* , vengono restituite solo le informazioni sull'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="06997-107">If the *StorageAccountName* parameter is specified, then only information about the specified storage account is returned.</span></span>

## <span data-ttu-id="06997-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06997-108">EXAMPLES</span></span>

### <span data-ttu-id="06997-109">Esempio 1: restituire tutti gli account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="06997-109">Example 1: Return all storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount
```

<span data-ttu-id="06997-110">Questo comando restituisce un oggetto con tutti gli account di archiviazione associati alla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="06997-110">This command returns an object with all the storage accounts associated with the current subscription.</span></span>

### <span data-ttu-id="06997-111">Esempio 2: restituire le informazioni sull'account per un account specificato</span><span class="sxs-lookup"><span data-stu-id="06997-111">Example 2: Return account information for a specified account</span></span>
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="06997-112">Questo comando restituisce un oggetto con solo le informazioni dell'account ContosoStore01.</span><span class="sxs-lookup"><span data-stu-id="06997-112">This command returns an object with only the ContosoStore01 account information.</span></span>

### <span data-ttu-id="06997-113">Esempio 3: visualizzare una tabella di account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="06997-113">Example 3: Display a table of storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

<span data-ttu-id="06997-114">Questo comando restituisce un oggetto con tutti gli account di archiviazione associati alla sottoscrizione corrente e li Visualizza come tabella che mostra il nome dell'account, l'etichetta dell'account e la posizione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="06997-114">This command returns an object with all the storage accounts associated with the current subscription, and outputs them as a table showing the account name, the account label, and the storage location.</span></span>

## <span data-ttu-id="06997-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06997-115">PARAMETERS</span></span>

### <span data-ttu-id="06997-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="06997-116">-InformationAction</span></span>
<span data-ttu-id="06997-117">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="06997-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="06997-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="06997-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06997-119">Continuare</span><span class="sxs-lookup"><span data-stu-id="06997-119">Continue</span></span>
- <span data-ttu-id="06997-120">Ignora</span><span class="sxs-lookup"><span data-stu-id="06997-120">Ignore</span></span>
- <span data-ttu-id="06997-121">Informarsi</span><span class="sxs-lookup"><span data-stu-id="06997-121">Inquire</span></span>
- <span data-ttu-id="06997-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="06997-122">SilentlyContinue</span></span>
- <span data-ttu-id="06997-123">Stop</span><span class="sxs-lookup"><span data-stu-id="06997-123">Stop</span></span>
- <span data-ttu-id="06997-124">Sospensione</span><span class="sxs-lookup"><span data-stu-id="06997-124">Suspend</span></span>

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

### <span data-ttu-id="06997-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="06997-125">-InformationVariable</span></span>
<span data-ttu-id="06997-126">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="06997-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="06997-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="06997-127">-Profile</span></span>
<span data-ttu-id="06997-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06997-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="06997-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="06997-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06997-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="06997-130">-StorageAccountName</span></span>
<span data-ttu-id="06997-131">Specifica il nome di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="06997-131">Specifies the name of a storage account.</span></span>
<span data-ttu-id="06997-132">Se specificato, questo cmdlet restituisce solo l'oggetto account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="06997-132">If specified, this cmdlet returns only the specified storage account object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06997-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06997-133">CommonParameters</span></span>
<span data-ttu-id="06997-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06997-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06997-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06997-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06997-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06997-136">INPUTS</span></span>

## <span data-ttu-id="06997-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06997-137">OUTPUTS</span></span>

### <span data-ttu-id="06997-138">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="06997-138">ManagementOperationContext</span></span>

## <span data-ttu-id="06997-139">Note</span><span class="sxs-lookup"><span data-stu-id="06997-139">NOTES</span></span>
* <span data-ttu-id="06997-140">Digitare `help node-dev` per ottenere assistenza per Node.js cmdlet correlati allo sviluppo.</span><span class="sxs-lookup"><span data-stu-id="06997-140">Type `help node-dev` to get help on Node.js development-related cmdlets.</span></span> <span data-ttu-id="06997-141">Digitare `help php-dev` per ottenere assistenza per i cmdlet correlati allo sviluppo php.</span><span class="sxs-lookup"><span data-stu-id="06997-141">Type `help php-dev` to get help on PHP development-related cmdlets.</span></span>

## <span data-ttu-id="06997-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06997-142">RELATED LINKS</span></span>

[<span data-ttu-id="06997-143">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="06997-143">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="06997-144">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="06997-144">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


