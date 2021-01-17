---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 75af40b104bbf6ffa65211087572140a070b71e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473567"
---
# <span data-ttu-id="7a35a-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7a35a-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="7a35a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a35a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a35a-103">Elimina definitivamente un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7a35a-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="7a35a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a35a-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a35a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a35a-105">DESCRIPTION</span></span>
<span data-ttu-id="7a35a-106">Il cmdlet **Remove-AzDataLakeStoreAccount** Elimina definitivamente un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7a35a-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="7a35a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a35a-107">EXAMPLES</span></span>

### <span data-ttu-id="7a35a-108">Esempio 1: rimuovere un account di data Lake Store</span><span class="sxs-lookup"><span data-stu-id="7a35a-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="7a35a-109">Questo comando rimuove l'account denominato ContosoADL da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7a35a-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="7a35a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a35a-110">PARAMETERS</span></span>

### <span data-ttu-id="7a35a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a35a-111">-DefaultProfile</span></span>
<span data-ttu-id="7a35a-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7a35a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a35a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7a35a-113">-Force</span></span>
<span data-ttu-id="7a35a-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7a35a-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a35a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a35a-115">-Name</span></span>
<span data-ttu-id="7a35a-116">Specifica il nome dell'account da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7a35a-116">Specifies the name of the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a35a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a35a-117">-PassThru</span></span>
<span data-ttu-id="7a35a-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="7a35a-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7a35a-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="7a35a-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a35a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a35a-120">-ResourceGroupName</span></span>
<span data-ttu-id="7a35a-121">Specifica il gruppo di risorse che contiene l'account da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7a35a-121">Specifies the resource group that contains the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a35a-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7a35a-122">-Confirm</span></span>
<span data-ttu-id="7a35a-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a35a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a35a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a35a-124">-WhatIf</span></span>
<span data-ttu-id="7a35a-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a35a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a35a-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a35a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a35a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a35a-127">CommonParameters</span></span>
<span data-ttu-id="7a35a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a35a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a35a-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a35a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a35a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a35a-130">INPUTS</span></span>

### <span data-ttu-id="7a35a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7a35a-131">System.String</span></span>

## <span data-ttu-id="7a35a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a35a-132">OUTPUTS</span></span>

### <span data-ttu-id="7a35a-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7a35a-133">System.Boolean</span></span>

## <span data-ttu-id="7a35a-134">Note</span><span class="sxs-lookup"><span data-stu-id="7a35a-134">NOTES</span></span>

## <span data-ttu-id="7a35a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a35a-135">RELATED LINKS</span></span>

[<span data-ttu-id="7a35a-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7a35a-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="7a35a-137">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7a35a-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="7a35a-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7a35a-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="7a35a-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7a35a-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


