---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: e12f69cbb36c5fabccffc4102723175c9f6b8909
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992164"
---
# <span data-ttu-id="cffe0-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="cffe0-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="cffe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cffe0-102">SYNOPSIS</span></span>
<span data-ttu-id="cffe0-103">Crea una nuova configurazione per una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="cffe0-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="cffe0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cffe0-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cffe0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cffe0-105">DESCRIPTION</span></span>
<span data-ttu-id="cffe0-106">Il cmdlet New-AzSqlVMConfig crea un nuovo oggetto di configurazione per una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="cffe0-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="cffe0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cffe0-107">EXAMPLES</span></span>

### <span data-ttu-id="cffe0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cffe0-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="cffe0-109">Crea un oggetto configurabile locale della macchina virtuale SQL che può essere usato per creare una macchina virtuale SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="cffe0-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="cffe0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cffe0-110">PARAMETERS</span></span>

### <span data-ttu-id="cffe0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cffe0-111">-DefaultProfile</span></span>
<span data-ttu-id="cffe0-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cffe0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cffe0-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="cffe0-113">-LicenseType</span></span>
<span data-ttu-id="cffe0-114">SQL di licenza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cffe0-114">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffe0-115">-Offerta</span><span class="sxs-lookup"><span data-stu-id="cffe0-115">-Offer</span></span>
<span data-ttu-id="cffe0-116">SQL di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="cffe0-116">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffe0-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="cffe0-117">-Sku</span></span>
<span data-ttu-id="cffe0-118">SQL di edizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cffe0-118">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffe0-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="cffe0-119">-SqlManagementType</span></span>
<span data-ttu-id="cffe0-120">SQL di gestione delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="cffe0-120">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffe0-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="cffe0-121">-Tag</span></span>
<span data-ttu-id="cffe0-122">I tag da associare alla macchina SQL virtuale</span><span class="sxs-lookup"><span data-stu-id="cffe0-122">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffe0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cffe0-123">CommonParameters</span></span>
<span data-ttu-id="cffe0-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cffe0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cffe0-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cffe0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cffe0-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="cffe0-126">INPUTS</span></span>

### <span data-ttu-id="cffe0-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cffe0-127">None</span></span>

## <span data-ttu-id="cffe0-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cffe0-128">OUTPUTS</span></span>

### <span data-ttu-id="cffe0-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="cffe0-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="cffe0-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="cffe0-130">NOTES</span></span>

## <span data-ttu-id="cffe0-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cffe0-131">RELATED LINKS</span></span>
