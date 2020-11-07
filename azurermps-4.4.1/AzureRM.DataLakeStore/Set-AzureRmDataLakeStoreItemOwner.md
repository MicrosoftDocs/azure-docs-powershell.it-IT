---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: fc71ec338303876a2cff44a07632e9fae5d3d2d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688643"
---
# <span data-ttu-id="3c7d0-101">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="3c7d0-101">Set-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="3c7d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c7d0-102">SYNOPSIS</span></span>
<span data-ttu-id="3c7d0-103">Modifica il proprietario di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c7d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c7d0-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c7d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c7d0-105">DESCRIPTION</span></span>
<span data-ttu-id="3c7d0-106">Il cmdlet **set-AzureRmDataLakeStoreItemOwner** modifica il proprietario di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-106">The **Set-AzureRmDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3c7d0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c7d0-107">EXAMPLES</span></span>

### <span data-ttu-id="3c7d0-108">Esempio 1: impostare il proprietario per un elemento</span><span class="sxs-lookup"><span data-stu-id="3c7d0-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="3c7d0-109">Questo comando imposta il proprietario della directory radice su Patti Fuller.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="3c7d0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c7d0-110">PARAMETERS</span></span>

### <span data-ttu-id="3c7d0-111">-Account</span><span class="sxs-lookup"><span data-stu-id="3c7d0-111">-Account</span></span>
<span data-ttu-id="3c7d0-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3c7d0-113">-ID</span><span class="sxs-lookup"><span data-stu-id="3c7d0-113">-Id</span></span>
<span data-ttu-id="3c7d0-114">Specifica l'ID oggetto dell'utente della directory AzureActive, del gruppo o dell'entità del servizio da usare come proprietario.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-114">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7d0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c7d0-115">-PassThru</span></span>
<span data-ttu-id="3c7d0-116">Indica che deve essere restituito il proprietario aggiornato risultante.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-116">Indicates the resulting updated owner should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7d0-117">-Path</span><span class="sxs-lookup"><span data-stu-id="3c7d0-117">-Path</span></span>
<span data-ttu-id="3c7d0-118">Specifica il percorso dello Store Data Lake dell'elemento da modificare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="3c7d0-118">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="3c7d0-119">-Digitare</span><span class="sxs-lookup"><span data-stu-id="3c7d0-119">-Type</span></span>
<span data-ttu-id="3c7d0-120">Specifica il tipo di proprietario da impostare.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-120">Specifies the type of owner to set.</span></span>
<span data-ttu-id="3c7d0-121">I valori accettabili per questo parametro sono: utente e gruppo.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-121">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7d0-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3c7d0-122">-Confirm</span></span>
<span data-ttu-id="3c7d0-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7d0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c7d0-124">-WhatIf</span></span>
<span data-ttu-id="3c7d0-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c7d0-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7d0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c7d0-127">-DefaultProfile</span></span>
<span data-ttu-id="3c7d0-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c7d0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c7d0-129">CommonParameters</span></span>
<span data-ttu-id="3c7d0-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c7d0-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c7d0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c7d0-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c7d0-132">INPUTS</span></span>

## <span data-ttu-id="3c7d0-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c7d0-133">OUTPUTS</span></span>

### <span data-ttu-id="3c7d0-134">stringa</span><span class="sxs-lookup"><span data-stu-id="3c7d0-134">string</span></span>
<span data-ttu-id="3c7d0-135">Se PassThru è specificato, restituisce il proprietario aggiornato.</span><span class="sxs-lookup"><span data-stu-id="3c7d0-135">If PassThru is specified, returns the updated owner.</span></span>

## <span data-ttu-id="3c7d0-136">Note</span><span class="sxs-lookup"><span data-stu-id="3c7d0-136">NOTES</span></span>

## <span data-ttu-id="3c7d0-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c7d0-137">RELATED LINKS</span></span>

[<span data-ttu-id="3c7d0-138">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="3c7d0-138">Get-AzureRmDataLakeStoreItemOwner</span></span>](./Get-AzureRmDataLakeStoreItemOwner.md)


