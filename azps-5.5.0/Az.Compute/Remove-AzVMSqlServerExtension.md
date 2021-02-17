---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 599b4817ce9f4f6f1f7a75f5811c5a3122f1bbb7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210002"
---
# <span data-ttu-id="aea37-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="aea37-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="aea37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aea37-102">SYNOPSIS</span></span>
<span data-ttu-id="aea37-103">Rimuove un'SQL Server predefinita da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="aea37-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="aea37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aea37-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aea37-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aea37-105">DESCRIPTION</span></span>
<span data-ttu-id="aea37-106">Il cmdlet **Remove-AzVMSqlServerExtension rimuove** un'estensione del server AzureSQL da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="aea37-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="aea37-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aea37-107">EXAMPLES</span></span>

### <span data-ttu-id="aea37-108">Esempio 1: Rimuovere un'SQL Server predefinita</span><span class="sxs-lookup"><span data-stu-id="aea37-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="aea37-109">Questo comando rimuove un SQL Server dalla macchina virtuale ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="aea37-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="aea37-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aea37-110">PARAMETERS</span></span>

### <span data-ttu-id="aea37-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea37-111">-DefaultProfile</span></span>
<span data-ttu-id="aea37-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aea37-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aea37-113">-Name</span><span class="sxs-lookup"><span data-stu-id="aea37-113">-Name</span></span>
<span data-ttu-id="aea37-114">Specifica il nome dell'SQL Server'estensione rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aea37-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="aea37-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aea37-115">-NoWait</span></span>
<span data-ttu-id="aea37-116">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="aea37-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="aea37-117">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="aea37-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="aea37-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea37-118">-ResourceGroupName</span></span>
<span data-ttu-id="aea37-119">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="aea37-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="aea37-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="aea37-120">-VMName</span></span>
<span data-ttu-id="aea37-121">Specifica il nome della macchina virtuale da cui questo cmdlet rimuove l SQL Server estensione.</span><span class="sxs-lookup"><span data-stu-id="aea37-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="aea37-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea37-122">CommonParameters</span></span>
<span data-ttu-id="aea37-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aea37-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea37-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aea37-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea37-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="aea37-125">INPUTS</span></span>

### <span data-ttu-id="aea37-126">System.String</span><span class="sxs-lookup"><span data-stu-id="aea37-126">System.String</span></span>

## <span data-ttu-id="aea37-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aea37-127">OUTPUTS</span></span>

### <span data-ttu-id="aea37-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="aea37-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="aea37-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="aea37-129">NOTES</span></span>

## <span data-ttu-id="aea37-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aea37-130">RELATED LINKS</span></span>

[<span data-ttu-id="aea37-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="aea37-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="aea37-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="aea37-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


