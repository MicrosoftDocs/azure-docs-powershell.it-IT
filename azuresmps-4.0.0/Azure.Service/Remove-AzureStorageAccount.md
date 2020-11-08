---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 679452A6-A6CA-4DC8-8E00-09E369505319
online version: ''
schema: 2.0.0
ms.openlocfilehash: 933c6de8e7baa55b2093a7ffc4ac28fede13bb5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029920"
---
# <span data-ttu-id="86f92-101">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86f92-101">Remove-AzureStorageAccount</span></span>

## <span data-ttu-id="86f92-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86f92-102">SYNOPSIS</span></span>
<span data-ttu-id="86f92-103">Elimina l'account di archiviazione specificato da un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="86f92-103">Deletes the specified storage account from a subscription.</span></span>

## <span data-ttu-id="86f92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86f92-104">SYNTAX</span></span>

```
Remove-AzureStorageAccount [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="86f92-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86f92-105">DESCRIPTION</span></span>
<span data-ttu-id="86f92-106">Il cmdlet **Remove-AzureStorageAccount** rimuove un account da un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="86f92-106">The **Remove-AzureStorageAccount** cmdlet removes an account from an Azure subscription.</span></span>

## <span data-ttu-id="86f92-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86f92-107">EXAMPLES</span></span>

### <span data-ttu-id="86f92-108">Esempio 1: rimuovere un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="86f92-108">Example 1: Remove a storage account</span></span>
```
PS C:\> Remove-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="86f92-109">Questo comando rimuove l'account di archiviazione di ContosoStore01 dall'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="86f92-109">This command removes the ContosoStore01 storage account from the specified subscription.</span></span>

## <span data-ttu-id="86f92-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86f92-110">PARAMETERS</span></span>

### <span data-ttu-id="86f92-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="86f92-111">-InformationAction</span></span>
<span data-ttu-id="86f92-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="86f92-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="86f92-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="86f92-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="86f92-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="86f92-114">Continue</span></span>
- <span data-ttu-id="86f92-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="86f92-115">Ignore</span></span>
- <span data-ttu-id="86f92-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="86f92-116">Inquire</span></span>
- <span data-ttu-id="86f92-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="86f92-117">SilentlyContinue</span></span>
- <span data-ttu-id="86f92-118">Stop</span><span class="sxs-lookup"><span data-stu-id="86f92-118">Stop</span></span>
- <span data-ttu-id="86f92-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="86f92-119">Suspend</span></span>

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

### <span data-ttu-id="86f92-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="86f92-120">-InformationVariable</span></span>
<span data-ttu-id="86f92-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="86f92-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="86f92-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="86f92-122">-Profile</span></span>
<span data-ttu-id="86f92-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86f92-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86f92-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="86f92-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86f92-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="86f92-125">-StorageAccountName</span></span>
<span data-ttu-id="86f92-126">Specifica il nome dell'account di archiviazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="86f92-126">Specifies the name of the storage account to remove.</span></span>

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

### <span data-ttu-id="86f92-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f92-127">CommonParameters</span></span>
<span data-ttu-id="86f92-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86f92-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f92-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86f92-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f92-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86f92-130">INPUTS</span></span>

## <span data-ttu-id="86f92-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86f92-131">OUTPUTS</span></span>

## <span data-ttu-id="86f92-132">Note</span><span class="sxs-lookup"><span data-stu-id="86f92-132">NOTES</span></span>

## <span data-ttu-id="86f92-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86f92-133">RELATED LINKS</span></span>

[<span data-ttu-id="86f92-134">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86f92-134">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="86f92-135">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86f92-135">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="86f92-136">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86f92-136">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


