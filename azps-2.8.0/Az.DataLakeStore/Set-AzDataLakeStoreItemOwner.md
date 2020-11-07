---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 446bd86eb37e45d3b4b302fdedf46e1cbe05e51c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674760"
---
# <span data-ttu-id="d7eda-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="d7eda-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="d7eda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7eda-102">SYNOPSIS</span></span>
<span data-ttu-id="d7eda-103">Modifica il proprietario di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7eda-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d7eda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7eda-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7eda-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7eda-105">DESCRIPTION</span></span>
<span data-ttu-id="d7eda-106">Il cmdlet **set-AzDataLakeStoreItemOwner** modifica il proprietario di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7eda-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d7eda-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7eda-107">EXAMPLES</span></span>

### <span data-ttu-id="d7eda-108">Esempio 1: impostare il proprietario per un elemento</span><span class="sxs-lookup"><span data-stu-id="d7eda-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="d7eda-109">Questo comando imposta il proprietario della directory radice su Patti Fuller.</span><span class="sxs-lookup"><span data-stu-id="d7eda-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="d7eda-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7eda-110">PARAMETERS</span></span>

### <span data-ttu-id="d7eda-111">-Account</span><span class="sxs-lookup"><span data-stu-id="d7eda-111">-Account</span></span>
<span data-ttu-id="d7eda-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7eda-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d7eda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7eda-113">-DefaultProfile</span></span>
<span data-ttu-id="d7eda-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7eda-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7eda-115">-ID</span><span class="sxs-lookup"><span data-stu-id="d7eda-115">-Id</span></span>
<span data-ttu-id="d7eda-116">Specifica l'ID oggetto dell'utente della directory AzureActive, del gruppo o dell'entità del servizio da usare come proprietario.</span><span class="sxs-lookup"><span data-stu-id="d7eda-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

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

### <span data-ttu-id="d7eda-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7eda-117">-PassThru</span></span>
<span data-ttu-id="d7eda-118">Indica che deve essere restituito il proprietario aggiornato risultante.</span><span class="sxs-lookup"><span data-stu-id="d7eda-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="d7eda-119">-Path</span><span class="sxs-lookup"><span data-stu-id="d7eda-119">-Path</span></span>
<span data-ttu-id="d7eda-120">Specifica il percorso dello Store Data Lake dell'elemento da modificare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="d7eda-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d7eda-121">-Digitare</span><span class="sxs-lookup"><span data-stu-id="d7eda-121">-Type</span></span>
<span data-ttu-id="d7eda-122">Specifica il tipo di proprietario da impostare.</span><span class="sxs-lookup"><span data-stu-id="d7eda-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="d7eda-123">I valori accettabili per questo parametro sono: utente e gruppo.</span><span class="sxs-lookup"><span data-stu-id="d7eda-123">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="d7eda-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d7eda-124">-Confirm</span></span>
<span data-ttu-id="d7eda-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7eda-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7eda-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7eda-126">-WhatIf</span></span>
<span data-ttu-id="d7eda-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7eda-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7eda-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7eda-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7eda-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7eda-129">CommonParameters</span></span>
<span data-ttu-id="d7eda-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7eda-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7eda-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7eda-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7eda-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7eda-132">INPUTS</span></span>

### <span data-ttu-id="d7eda-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d7eda-133">System.String</span></span>

### <span data-ttu-id="d7eda-134">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d7eda-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d7eda-135">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="d7eda-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="d7eda-136">System. Guid</span><span class="sxs-lookup"><span data-stu-id="d7eda-136">System.Guid</span></span>

### <span data-ttu-id="d7eda-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d7eda-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d7eda-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7eda-138">OUTPUTS</span></span>

### <span data-ttu-id="d7eda-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d7eda-139">System.String</span></span>

## <span data-ttu-id="d7eda-140">Note</span><span class="sxs-lookup"><span data-stu-id="d7eda-140">NOTES</span></span>

## <span data-ttu-id="d7eda-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7eda-141">RELATED LINKS</span></span>

[<span data-ttu-id="d7eda-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="d7eda-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


