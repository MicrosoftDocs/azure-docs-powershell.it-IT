---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 81acbdd914d4a3cdb69da9ac0d2093f4e1dd4cdf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675242"
---
# <span data-ttu-id="b2774-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b2774-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="b2774-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2774-102">SYNOPSIS</span></span>
<span data-ttu-id="b2774-103">Rimuove un'estensione di SQL Server da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2774-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="b2774-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2774-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2774-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2774-105">DESCRIPTION</span></span>
<span data-ttu-id="b2774-106">Il cmdlet **Remove-AzVMSqlServerExtension** rimuove un'estensione del server AzureSQL da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2774-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="b2774-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2774-107">EXAMPLES</span></span>

### <span data-ttu-id="b2774-108">Esempio 1: rimuovere un'estensione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="b2774-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="b2774-109">Questo comando rimuove un'estensione di SQL Server dalla macchina virtuale denominata ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="b2774-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="b2774-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2774-110">PARAMETERS</span></span>

### <span data-ttu-id="b2774-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2774-111">-DefaultProfile</span></span>
<span data-ttu-id="b2774-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2774-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2774-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2774-113">-Name</span></span>
<span data-ttu-id="b2774-114">Specifica il nome di SQL Server che viene rimosso dall'estensione di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2774-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b2774-115">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="b2774-115">-NoWait</span></span>
<span data-ttu-id="b2774-116">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b2774-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="b2774-117">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="b2774-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="b2774-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2774-118">-ResourceGroupName</span></span>
<span data-ttu-id="b2774-119">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2774-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b2774-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="b2774-120">-VMName</span></span>
<span data-ttu-id="b2774-121">Specifica il nome della macchina virtuale da cui questo cmdlet rimuove l'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b2774-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="b2774-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2774-122">CommonParameters</span></span>
<span data-ttu-id="b2774-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2774-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2774-124">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2774-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2774-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2774-125">INPUTS</span></span>

### <span data-ttu-id="b2774-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b2774-126">System.String</span></span>

## <span data-ttu-id="b2774-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2774-127">OUTPUTS</span></span>

### <span data-ttu-id="b2774-128">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b2774-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b2774-129">Note</span><span class="sxs-lookup"><span data-stu-id="b2774-129">NOTES</span></span>

## <span data-ttu-id="b2774-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2774-130">RELATED LINKS</span></span>

[<span data-ttu-id="b2774-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b2774-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="b2774-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b2774-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


