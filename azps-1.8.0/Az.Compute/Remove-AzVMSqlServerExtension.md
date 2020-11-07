---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 630df5bbe6677c7019d372a2a6977cc4c724a421
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684736"
---
# <span data-ttu-id="709be-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="709be-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="709be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="709be-102">SYNOPSIS</span></span>
<span data-ttu-id="709be-103">Rimuove un'estensione di SQL Server da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="709be-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="709be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="709be-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="709be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="709be-105">DESCRIPTION</span></span>
<span data-ttu-id="709be-106">Il cmdlet **Remove-AzVMSqlServerExtension** rimuove un'estensione del server AzureSQL da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="709be-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="709be-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="709be-107">EXAMPLES</span></span>

### <span data-ttu-id="709be-108">Esempio 1: rimuovere un'estensione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="709be-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="709be-109">Questo comando rimuove un'estensione di SQL Server dalla macchina virtuale denominata ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="709be-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="709be-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="709be-110">PARAMETERS</span></span>

### <span data-ttu-id="709be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709be-111">-DefaultProfile</span></span>
<span data-ttu-id="709be-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="709be-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="709be-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="709be-113">-Name</span></span>
<span data-ttu-id="709be-114">Specifica il nome di SQL Server che viene rimosso dall'estensione di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="709be-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="709be-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="709be-115">-ResourceGroupName</span></span>
<span data-ttu-id="709be-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="709be-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="709be-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="709be-117">-VMName</span></span>
<span data-ttu-id="709be-118">Specifica il nome della macchina virtuale da cui questo cmdlet rimuove l'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="709be-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="709be-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709be-119">CommonParameters</span></span>
<span data-ttu-id="709be-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="709be-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709be-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="709be-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709be-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="709be-122">INPUTS</span></span>

### <span data-ttu-id="709be-123">System. String</span><span class="sxs-lookup"><span data-stu-id="709be-123">System.String</span></span>

## <span data-ttu-id="709be-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="709be-124">OUTPUTS</span></span>

### <span data-ttu-id="709be-125">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="709be-125">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="709be-126">Note</span><span class="sxs-lookup"><span data-stu-id="709be-126">NOTES</span></span>

## <span data-ttu-id="709be-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="709be-127">RELATED LINKS</span></span>

[<span data-ttu-id="709be-128">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="709be-128">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="709be-129">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="709be-129">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


