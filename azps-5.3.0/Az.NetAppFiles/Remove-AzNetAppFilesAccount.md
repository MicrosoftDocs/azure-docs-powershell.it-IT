---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f6e2421a20cb7aaf044d3abfbbddf7f5c72b37e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486800"
---
# <span data-ttu-id="d2e41-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d2e41-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="d2e41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2e41-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e41-103">Elimina un account di ANF (Azure NetApp files).</span><span class="sxs-lookup"><span data-stu-id="d2e41-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="d2e41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2e41-104">SYNTAX</span></span>

### <span data-ttu-id="d2e41-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d2e41-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2e41-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2e41-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2e41-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2e41-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2e41-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2e41-108">DESCRIPTION</span></span>
<span data-ttu-id="d2e41-109">Il cmdlet **Remove-AzNetAppFilesAccount** Elimina un account ANF.</span><span class="sxs-lookup"><span data-stu-id="d2e41-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="d2e41-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2e41-110">EXAMPLES</span></span>

### <span data-ttu-id="d2e41-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d2e41-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="d2e41-112">Questo comando Elimina l'account di ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="d2e41-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="d2e41-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2e41-113">PARAMETERS</span></span>

### <span data-ttu-id="d2e41-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e41-114">-DefaultProfile</span></span>
<span data-ttu-id="d2e41-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e41-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2e41-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2e41-116">-InputObject</span></span>
<span data-ttu-id="d2e41-117">Oggetto account da rimuovere</span><span class="sxs-lookup"><span data-stu-id="d2e41-117">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e41-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2e41-118">-Name</span></span>
<span data-ttu-id="d2e41-119">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="d2e41-119">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e41-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2e41-120">-PassThru</span></span>
<span data-ttu-id="d2e41-121">Restituisce se l'account specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="d2e41-121">Return whether the specified account was successfully removed</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e41-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e41-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2e41-123">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="d2e41-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e41-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2e41-124">-ResourceId</span></span>
<span data-ttu-id="d2e41-125">ID risorsa dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="d2e41-125">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e41-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2e41-126">-Confirm</span></span>
<span data-ttu-id="d2e41-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2e41-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2e41-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2e41-128">-WhatIf</span></span>
<span data-ttu-id="d2e41-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2e41-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2e41-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2e41-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2e41-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e41-131">CommonParameters</span></span>
<span data-ttu-id="d2e41-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2e41-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e41-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2e41-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e41-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2e41-134">INPUTS</span></span>

### <span data-ttu-id="d2e41-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d2e41-135">System.String</span></span>

### <span data-ttu-id="d2e41-136">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d2e41-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d2e41-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2e41-137">OUTPUTS</span></span>

### <span data-ttu-id="d2e41-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2e41-138">System.Boolean</span></span>

## <span data-ttu-id="d2e41-139">Note</span><span class="sxs-lookup"><span data-stu-id="d2e41-139">NOTES</span></span>

## <span data-ttu-id="d2e41-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2e41-140">RELATED LINKS</span></span>
