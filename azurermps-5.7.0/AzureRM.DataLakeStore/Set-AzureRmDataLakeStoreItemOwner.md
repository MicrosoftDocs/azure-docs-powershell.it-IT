---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 4806c4c25ac6fecce4961ef5d4ffe44daa1ae8f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519472"
---
# <span data-ttu-id="c9db6-101">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="c9db6-101">Set-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="c9db6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9db6-102">SYNOPSIS</span></span>
<span data-ttu-id="c9db6-103">Modifica il proprietario di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c9db6-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9db6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9db6-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9db6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9db6-105">DESCRIPTION</span></span>
<span data-ttu-id="c9db6-106">Il cmdlet **set-AzureRmDataLakeStoreItemOwner** modifica il proprietario di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c9db6-106">The **Set-AzureRmDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c9db6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9db6-107">EXAMPLES</span></span>

### <span data-ttu-id="c9db6-108">Esempio 1: impostare il proprietario per un elemento</span><span class="sxs-lookup"><span data-stu-id="c9db6-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="c9db6-109">Questo comando imposta il proprietario della directory radice su Patti Fuller.</span><span class="sxs-lookup"><span data-stu-id="c9db6-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="c9db6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9db6-110">PARAMETERS</span></span>

### <span data-ttu-id="c9db6-111">-Account</span><span class="sxs-lookup"><span data-stu-id="c9db6-111">-Account</span></span>
<span data-ttu-id="c9db6-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c9db6-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9db6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9db6-113">-DefaultProfile</span></span>
<span data-ttu-id="c9db6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9db6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9db6-115">-ID</span><span class="sxs-lookup"><span data-stu-id="c9db6-115">-Id</span></span>
<span data-ttu-id="c9db6-116">Specifica l'ID oggetto dell'utente della directory AzureActive, del gruppo o dell'entità del servizio da usare come proprietario.</span><span class="sxs-lookup"><span data-stu-id="c9db6-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9db6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9db6-117">-PassThru</span></span>
<span data-ttu-id="c9db6-118">Indica che deve essere restituito il proprietario aggiornato risultante.</span><span class="sxs-lookup"><span data-stu-id="c9db6-118">Indicates the resulting updated owner should be returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9db6-119">-Path</span><span class="sxs-lookup"><span data-stu-id="c9db6-119">-Path</span></span>
<span data-ttu-id="c9db6-120">Specifica il percorso dello Store Data Lake dell'elemento da modificare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="c9db6-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9db6-121">-Digitare</span><span class="sxs-lookup"><span data-stu-id="c9db6-121">-Type</span></span>
<span data-ttu-id="c9db6-122">Specifica il tipo di proprietario da impostare.</span><span class="sxs-lookup"><span data-stu-id="c9db6-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="c9db6-123">I valori accettabili per questo parametro sono: utente e gruppo.</span><span class="sxs-lookup"><span data-stu-id="c9db6-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Owner
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9db6-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c9db6-124">-Confirm</span></span>
<span data-ttu-id="c9db6-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9db6-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9db6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9db6-126">-WhatIf</span></span>
<span data-ttu-id="c9db6-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9db6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9db6-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9db6-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9db6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9db6-129">CommonParameters</span></span>
<span data-ttu-id="c9db6-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9db6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9db6-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9db6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9db6-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9db6-132">INPUTS</span></span>

### <span data-ttu-id="c9db6-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c9db6-133">None</span></span>
<span data-ttu-id="c9db6-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c9db6-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9db6-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9db6-135">OUTPUTS</span></span>

### <span data-ttu-id="c9db6-136">stringa</span><span class="sxs-lookup"><span data-stu-id="c9db6-136">string</span></span>
<span data-ttu-id="c9db6-137">Se PassThru è specificato, restituisce il proprietario aggiornato.</span><span class="sxs-lookup"><span data-stu-id="c9db6-137">If PassThru is specified, returns the updated owner.</span></span>

## <span data-ttu-id="c9db6-138">Note</span><span class="sxs-lookup"><span data-stu-id="c9db6-138">NOTES</span></span>

## <span data-ttu-id="c9db6-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9db6-139">RELATED LINKS</span></span>

[<span data-ttu-id="c9db6-140">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="c9db6-140">Get-AzureRmDataLakeStoreItemOwner</span></span>](./Get-AzureRmDataLakeStoreItemOwner.md)


