---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: f71c26e69f9f297a23d4e6902ca6aaac6b135c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522140"
---
# <span data-ttu-id="16d40-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="16d40-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="16d40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16d40-102">SYNOPSIS</span></span>
<span data-ttu-id="16d40-103">Imposta o rimuove il tempo di scadenza per un file in un account di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="16d40-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16d40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16d40-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16d40-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16d40-105">DESCRIPTION</span></span>
<span data-ttu-id="16d40-106">Il cmdlet **set-AzureRmDataLakeStoreItemExpiry** imposta o rimuove il tempo di scadenza per un file in un account di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="16d40-106">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="16d40-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16d40-107">EXAMPLES</span></span>

### <span data-ttu-id="16d40-108">Esempio 1: impostare la data di scadenza per un file</span><span class="sxs-lookup"><span data-stu-id="16d40-108">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="16d40-109">Imposta la scadenza nel file myfile.txt in account ContosoADL da due ore da ora.</span><span class="sxs-lookup"><span data-stu-id="16d40-109">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="16d40-110">In questo modo il file scadrà (contrassegnato per Delete) in due ore.</span><span class="sxs-lookup"><span data-stu-id="16d40-110">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="16d40-111">Esempio 2: rimuovere la scadenza in un file</span><span class="sxs-lookup"><span data-stu-id="16d40-111">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="16d40-112">Rimuove la scadenza precedentemente impostata sul file "myfile.txt" nell'account "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="16d40-112">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="16d40-113">Questo significa che il file non scadrà automaticamente (da contrassegnare per l'eliminazione) e dovrà essere eliminato manualmente o impostato in modo che scada di nuovo.</span><span class="sxs-lookup"><span data-stu-id="16d40-113">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

## <span data-ttu-id="16d40-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16d40-114">PARAMETERS</span></span>

### <span data-ttu-id="16d40-115">-Account</span><span class="sxs-lookup"><span data-stu-id="16d40-115">-Account</span></span>
<span data-ttu-id="16d40-116">Specifica il nome dell'account Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="16d40-116">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d40-117">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="16d40-117">-Expiration</span></span>
<span data-ttu-id="16d40-118">Ora di scadenza assoluta per il file specificato.</span><span class="sxs-lookup"><span data-stu-id="16d40-118">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="16d40-119">Se nessun valore o impostato su MaxValue, il file non scadrà mai.</span><span class="sxs-lookup"><span data-stu-id="16d40-119">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d40-120">-Path</span><span class="sxs-lookup"><span data-stu-id="16d40-120">-Path</span></span>
<span data-ttu-id="16d40-121">Specifica il percorso dello Store Data Lake dell'elemento file per il quale impostare o rimuovere la scadenza.</span><span class="sxs-lookup"><span data-stu-id="16d40-121">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d40-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="16d40-122">-Confirm</span></span>
<span data-ttu-id="16d40-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16d40-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d40-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16d40-124">-WhatIf</span></span>
<span data-ttu-id="16d40-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16d40-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16d40-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16d40-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d40-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d40-127">-DefaultProfile</span></span>
<span data-ttu-id="16d40-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16d40-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d40-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d40-129">CommonParameters</span></span>
<span data-ttu-id="16d40-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16d40-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d40-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16d40-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d40-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16d40-132">INPUTS</span></span>

## <span data-ttu-id="16d40-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16d40-133">OUTPUTS</span></span>

### <span data-ttu-id="16d40-134">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="16d40-134">DataLakeStoreItem</span></span>
<span data-ttu-id="16d40-135">Il file aggiornato con una nuova data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="16d40-135">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="16d40-136">Note</span><span class="sxs-lookup"><span data-stu-id="16d40-136">NOTES</span></span>
<span data-ttu-id="16d40-137">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="16d40-137">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="16d40-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16d40-138">RELATED LINKS</span></span>

[<span data-ttu-id="16d40-139">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="16d40-139">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

