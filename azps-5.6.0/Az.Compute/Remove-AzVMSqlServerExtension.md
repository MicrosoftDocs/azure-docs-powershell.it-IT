---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 42fb10ef388fdda9616f78453163db822da9d036
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985220"
---
# <span data-ttu-id="9c652-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9c652-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="9c652-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c652-102">SYNOPSIS</span></span>
<span data-ttu-id="9c652-103">Rimuove un'SQL Server predefinita da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9c652-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="9c652-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c652-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c652-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9c652-105">DESCRIPTION</span></span>
<span data-ttu-id="9c652-106">Il cmdlet **Remove-AzVMSqlServerExtension rimuove** un'estensione del server AzureSQL da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9c652-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="9c652-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c652-107">EXAMPLES</span></span>

### <span data-ttu-id="9c652-108">Esempio 1: Rimuovere un'SQL Server predefinita</span><span class="sxs-lookup"><span data-stu-id="9c652-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="9c652-109">Questo comando rimuove un SQL Server dalla macchina virtuale contosoVM22.</span><span class="sxs-lookup"><span data-stu-id="9c652-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="9c652-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c652-110">PARAMETERS</span></span>

### <span data-ttu-id="9c652-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c652-111">-DefaultProfile</span></span>
<span data-ttu-id="9c652-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c652-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c652-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9c652-113">-Name</span></span>
<span data-ttu-id="9c652-114">Specifica il nome dell'SQL Server'estensione rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c652-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9c652-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9c652-115">-NoWait</span></span>
<span data-ttu-id="9c652-116">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9c652-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9c652-117">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="9c652-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="9c652-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c652-118">-ResourceGroupName</span></span>
<span data-ttu-id="9c652-119">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9c652-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9c652-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="9c652-120">-VMName</span></span>
<span data-ttu-id="9c652-121">Specifica il nome della macchina virtuale da cui questo cmdlet rimuove l SQL Server estensione.</span><span class="sxs-lookup"><span data-stu-id="9c652-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="9c652-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c652-122">CommonParameters</span></span>
<span data-ttu-id="9c652-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c652-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c652-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c652-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c652-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="9c652-125">INPUTS</span></span>

### <span data-ttu-id="9c652-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9c652-126">System.String</span></span>

## <span data-ttu-id="9c652-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c652-127">OUTPUTS</span></span>

### <span data-ttu-id="9c652-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9c652-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9c652-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="9c652-129">NOTES</span></span>

## <span data-ttu-id="9c652-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c652-130">RELATED LINKS</span></span>

[<span data-ttu-id="9c652-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9c652-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="9c652-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9c652-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


