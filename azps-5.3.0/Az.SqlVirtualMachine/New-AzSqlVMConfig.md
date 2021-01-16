---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476636"
---
# <span data-ttu-id="22811-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="22811-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="22811-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22811-102">SYNOPSIS</span></span>
<span data-ttu-id="22811-103">Crea una nuova configurazione per una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="22811-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="22811-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22811-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22811-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22811-105">DESCRIPTION</span></span>
<span data-ttu-id="22811-106">Il cmdlet New-AzSqlVMConfig crea un nuovo oggetto di configurazione per una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="22811-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="22811-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22811-107">EXAMPLES</span></span>

### <span data-ttu-id="22811-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22811-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="22811-109">Crea un oggetto configurabile locale di una macchina virtuale SQL che può essere usato per creare una macchina virtuale di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="22811-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="22811-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22811-110">PARAMETERS</span></span>

### <span data-ttu-id="22811-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22811-111">-DefaultProfile</span></span>
<span data-ttu-id="22811-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22811-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22811-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="22811-113">-LicenseType</span></span>
<span data-ttu-id="22811-114">Tipo di licenza per la macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="22811-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="22811-115">-Offerta</span><span class="sxs-lookup"><span data-stu-id="22811-115">-Offer</span></span>
<span data-ttu-id="22811-116">Offerta macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="22811-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="22811-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="22811-117">-Sku</span></span>
<span data-ttu-id="22811-118">Tipo SQL Virtual Machine Edition.</span><span class="sxs-lookup"><span data-stu-id="22811-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="22811-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="22811-119">-SqlManagementType</span></span>
<span data-ttu-id="22811-120">Tipo di gestione della macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="22811-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="22811-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="22811-121">-Tag</span></span>
<span data-ttu-id="22811-122">Tag da associare alla macchina virtuale SQL</span><span class="sxs-lookup"><span data-stu-id="22811-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="22811-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22811-123">CommonParameters</span></span>
<span data-ttu-id="22811-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22811-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22811-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22811-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22811-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22811-126">INPUTS</span></span>

### <span data-ttu-id="22811-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="22811-127">None</span></span>

## <span data-ttu-id="22811-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22811-128">OUTPUTS</span></span>

### <span data-ttu-id="22811-129">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="22811-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="22811-130">Note</span><span class="sxs-lookup"><span data-stu-id="22811-130">NOTES</span></span>

## <span data-ttu-id="22811-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22811-131">RELATED LINKS</span></span>
