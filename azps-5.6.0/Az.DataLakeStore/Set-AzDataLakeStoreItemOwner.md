---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 37dbb1c81de0f7537dd708dc39b2356edfa46f6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995594"
---
# <span data-ttu-id="593e5-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="593e5-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="593e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="593e5-102">SYNOPSIS</span></span>
<span data-ttu-id="593e5-103">Modifica il proprietario di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="593e5-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="593e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="593e5-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="593e5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="593e5-105">DESCRIPTION</span></span>
<span data-ttu-id="593e5-106">Il cmdlet **Set-AzDataLakeStoreItemOwner** modifica il proprietario di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="593e5-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="593e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="593e5-107">EXAMPLES</span></span>

### <span data-ttu-id="593e5-108">Esempio 1: Impostare il proprietario di un elemento</span><span class="sxs-lookup"><span data-stu-id="593e5-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="593e5-109">Questo comando imposta il proprietario della directory radice su Patti Fuller.</span><span class="sxs-lookup"><span data-stu-id="593e5-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="593e5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="593e5-110">PARAMETERS</span></span>

### <span data-ttu-id="593e5-111">-Account</span><span class="sxs-lookup"><span data-stu-id="593e5-111">-Account</span></span>
<span data-ttu-id="593e5-112">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="593e5-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="593e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="593e5-113">-DefaultProfile</span></span>
<span data-ttu-id="593e5-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="593e5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="593e5-115">-Id</span><span class="sxs-lookup"><span data-stu-id="593e5-115">-Id</span></span>
<span data-ttu-id="593e5-116">Specifica l'ID oggetto dell'utente, gruppo o entità servizio di AzureActive Directory da usare come proprietario.</span><span class="sxs-lookup"><span data-stu-id="593e5-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

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

### <span data-ttu-id="593e5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="593e5-117">-PassThru</span></span>
<span data-ttu-id="593e5-118">Indica che il proprietario aggiornato risultante deve essere restituito.</span><span class="sxs-lookup"><span data-stu-id="593e5-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="593e5-119">-Path</span><span class="sxs-lookup"><span data-stu-id="593e5-119">-Path</span></span>
<span data-ttu-id="593e5-120">Specifica il percorso Data Lake Store dell'elemento da modificare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="593e5-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="593e5-121">-Type</span><span class="sxs-lookup"><span data-stu-id="593e5-121">-Type</span></span>
<span data-ttu-id="593e5-122">Specifica il tipo di proprietario da impostare.</span><span class="sxs-lookup"><span data-stu-id="593e5-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="593e5-123">I valori accettabili per questo parametro sono: Utente e Gruppo.</span><span class="sxs-lookup"><span data-stu-id="593e5-123">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="593e5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="593e5-124">-Confirm</span></span>
<span data-ttu-id="593e5-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="593e5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="593e5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="593e5-126">-WhatIf</span></span>
<span data-ttu-id="593e5-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="593e5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="593e5-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="593e5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="593e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="593e5-129">CommonParameters</span></span>
<span data-ttu-id="593e5-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="593e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="593e5-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="593e5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="593e5-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="593e5-132">INPUTS</span></span>

### <span data-ttu-id="593e5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="593e5-133">System.String</span></span>

### <span data-ttu-id="593e5-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="593e5-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="593e5-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span><span class="sxs-lookup"><span data-stu-id="593e5-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="593e5-136">System.Guid</span><span class="sxs-lookup"><span data-stu-id="593e5-136">System.Guid</span></span>

### <span data-ttu-id="593e5-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="593e5-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="593e5-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="593e5-138">OUTPUTS</span></span>

### <span data-ttu-id="593e5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="593e5-139">System.String</span></span>

## <span data-ttu-id="593e5-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="593e5-140">NOTES</span></span>

## <span data-ttu-id="593e5-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="593e5-141">RELATED LINKS</span></span>

[<span data-ttu-id="593e5-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="593e5-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


