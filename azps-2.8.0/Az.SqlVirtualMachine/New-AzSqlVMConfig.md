---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: a2ee91815553b1de6ae21eb2afb344e010058deb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857645"
---
# <span data-ttu-id="7395e-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="7395e-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="7395e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7395e-102">SYNOPSIS</span></span>
<span data-ttu-id="7395e-103">Crea una nuova configurazione per una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="7395e-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="7395e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7395e-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7395e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7395e-105">DESCRIPTION</span></span>
<span data-ttu-id="7395e-106">Il cmdlet New-AzSqlVMConfig crea un nuovo oggetto di configurazione per una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="7395e-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="7395e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7395e-107">EXAMPLES</span></span>

### <span data-ttu-id="7395e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7395e-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="7395e-109">Crea un oggetto configurabile locale di una macchina virtuale SQL che può essere usato per creare una macchina virtuale di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7395e-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="7395e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7395e-110">PARAMETERS</span></span>

### <span data-ttu-id="7395e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7395e-111">-DefaultProfile</span></span>
<span data-ttu-id="7395e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7395e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7395e-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7395e-113">-LicenseType</span></span>
<span data-ttu-id="7395e-114">Tipo di licenza per la macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="7395e-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="7395e-115">-Offerta</span><span class="sxs-lookup"><span data-stu-id="7395e-115">-Offer</span></span>
<span data-ttu-id="7395e-116">Offerta macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="7395e-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="7395e-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="7395e-117">-Sku</span></span>
<span data-ttu-id="7395e-118">Tipo SQL Virtual Machine Edition.</span><span class="sxs-lookup"><span data-stu-id="7395e-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="7395e-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="7395e-119">-SqlManagementType</span></span>
<span data-ttu-id="7395e-120">Tipo di gestione della macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="7395e-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="7395e-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="7395e-121">-Tag</span></span>
<span data-ttu-id="7395e-122">Tag da associare alla macchina virtuale SQL</span><span class="sxs-lookup"><span data-stu-id="7395e-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="7395e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7395e-123">CommonParameters</span></span>
<span data-ttu-id="7395e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7395e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7395e-125">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7395e-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7395e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7395e-126">INPUTS</span></span>

### <span data-ttu-id="7395e-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7395e-127">None</span></span>

## <span data-ttu-id="7395e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7395e-128">OUTPUTS</span></span>

### <span data-ttu-id="7395e-129">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7395e-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7395e-130">Note</span><span class="sxs-lookup"><span data-stu-id="7395e-130">NOTES</span></span>

## <span data-ttu-id="7395e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7395e-131">RELATED LINKS</span></span>
