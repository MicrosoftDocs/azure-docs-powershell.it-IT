---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 19d4022fcf5f3eee0ee8d77e7c061ae2f8d00629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521263"
---
# <span data-ttu-id="fdb07-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fdb07-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="fdb07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdb07-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb07-103">Rimuove un'estensione di SQL Server da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fdb07-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdb07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdb07-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdb07-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdb07-105">DESCRIPTION</span></span>
<span data-ttu-id="fdb07-106">Il cmdlet **Remove-AzureRmVMSqlServerExtension** rimuove un'estensione del server AzureSQL da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fdb07-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="fdb07-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdb07-107">EXAMPLES</span></span>

### <span data-ttu-id="fdb07-108">Esempio 1: rimuovere un'estensione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="fdb07-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="fdb07-109">Questo comando rimuove un'estensione di SQL Server dalla macchina virtuale denominata ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="fdb07-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="fdb07-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdb07-110">PARAMETERS</span></span>

### <span data-ttu-id="fdb07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb07-111">-DefaultProfile</span></span>
<span data-ttu-id="fdb07-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb07-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb07-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdb07-113">-Name</span></span>
<span data-ttu-id="fdb07-114">Specifica il nome di SQL Server che viene rimosso dall'estensione di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdb07-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fdb07-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb07-115">-ResourceGroupName</span></span>
<span data-ttu-id="fdb07-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fdb07-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fdb07-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="fdb07-117">-VMName</span></span>
<span data-ttu-id="fdb07-118">Specifica il nome della macchina virtuale da cui questo cmdlet rimuove l'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fdb07-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="fdb07-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb07-119">CommonParameters</span></span>
<span data-ttu-id="fdb07-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb07-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb07-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb07-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb07-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdb07-122">INPUTS</span></span>

## <span data-ttu-id="fdb07-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdb07-123">OUTPUTS</span></span>

## <span data-ttu-id="fdb07-124">Note</span><span class="sxs-lookup"><span data-stu-id="fdb07-124">NOTES</span></span>

## <span data-ttu-id="fdb07-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdb07-125">RELATED LINKS</span></span>

[<span data-ttu-id="fdb07-126">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fdb07-126">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="fdb07-127">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fdb07-127">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)

